# Repository History and File-Tree Notes

## `lafs-web-full` investigation

The repository history was checked specifically for a path named `lafs-web-full`.

### Findings

- The exact path `lafs-web-full` is **not present on the current `main` tree**.
- The exact path is also **not present in the file tree checked at the July 2026 Docker/Compose stage**.
- Direct GitHub content lookups for `lafs-web-full` at commits `3892b52f` and `6e6bb063` return `404 Not Found`, which means GitHub does not have that path at those revisions.
- The repository contains a Docker Compose service named **`lafs-web`**, but that is a container/service name, not a directory named `lafs-web-full`.
- No branch currently exposed by the repository is named for `lafs-web-full`; the repository currently exposes `main` plus the maintenance branch used for these cleanup changes.

### What the history shows

The July 12, 2026 commits added the Docker frontend configuration directly at the repository root. The Docker Compose configuration defines:

```yaml
services:
  app:
    container_name: lafs-web
```

This can make `lafs-web` appear as an application/container identifier even though there is no `lafs-web-full` directory in the Git tree.

Later, the repository was converted into a CS-470 portfolio-style repository. The merge commit `200f513c` combined the application with portfolio documentation and replaced the inherited tutorial-style README with CS-470 documentation.

## Conclusion

Based on the Git objects and file trees that are available in this repository, there is **no evidence that a Git-tracked `lafs-web-full` directory was later deleted or renamed**. The stronger explanation is that the folder existed locally during development or was referenced outside the tracked Git tree, while the GitHub repository itself tracked the Angular application at the repository root.

If a local PowerShell upload contained a folder named `lafs-web-full`, it was not represented as that path in the GitHub revisions inspected here.

## Cleanup performed

The repository cleanup branch also:

- Corrects the project metadata name in `package.json`.
- Aligns the Dockerfile's globally installed Angular CLI with the Angular 7 project dependencies.
- Removes the tracked Firebase cache artifact that was already covered by `.gitignore`.
- Keeps academic screenshots/evidence because they document the course work.
- Improves the README so the application, cloud work, documentation, and repository structure are clear to a reviewer.
