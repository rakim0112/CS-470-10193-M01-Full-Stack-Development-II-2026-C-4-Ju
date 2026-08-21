# CS-470 Full Stack Development II

## Cloud-Based Full-Stack Application Portfolio

**Student:** Rakim Spriggs  
**Course:** CS-470 Full Stack Development II  
**Term:** 2026 C-4  
**Program:** B.S. Computer Science, Southern New Hampshire University

---

## Project Overview

This repository contains my CS-470 work for extending a full-stack web application toward a cloud deployment model. The project builds on the application foundation from CS-465 and focuses on containerization, cloud services, deployment configuration, REST APIs, and troubleshooting across development and cloud environments.

The repository is intentionally organized as both a **working application** and an **academic portfolio artifact**. The application source remains in the original Angular project structure, while the `docs/` and `portfolio/` directories contain supporting documentation and presentation material.

## Technology Stack

| Area | Technology |
|---|---|
| Frontend | Angular 7 |
| UI | Angular Material, Bootstrap Sass, Font Awesome |
| Language | TypeScript |
| API integration | HTTP / REST |
| Backend foundation | Node.js / Express |
| Database foundation | MongoDB |
| Cloud | Amazon Web Services (AWS) |
| Static hosting | Amazon S3 |
| Serverless | AWS Lambda |
| Integration | CORS |
| Containers | Docker / Docker Compose |
| Version control | Git / GitHub |

## Architecture

The application follows a separated frontend, API, and database design. Docker provides a repeatable development environment, while AWS services support the cloud portion of the project.

```text
                    User
                      |
                      v
              Angular Frontend
                      |
                  HTTP / REST
                      |
                      v
            Node.js / Express API
                      |
                      v
                   MongoDB

Cloud deployment/support:
Angular production build --> Amazon S3
Serverless/API work ------> AWS Lambda
Browser/API integration --> CORS
Local containerization ---> Docker / Docker Compose
```

See [`docs/cloud-architecture.md`](docs/cloud-architecture.md) for the detailed architecture notes.

## Repository Structure

```text
.
├── docs/                 # Architecture, AWS, API, testing, and presentation notes
├── portfolio/            # Portfolio checklist and resume-oriented project summary
├── src/                  # Angular application source
├── sdk/                  # Generated/Supporting SDK code used by the application
├── e2e/                  # End-to-end testing configuration and specs
├── Dockerfile            # Container definition for the Angular application
├── docker-compose.yml    # Local Docker orchestration
├── angular.json          # Angular CLI project configuration
├── package.json          # Project metadata and npm scripts
└── package-lock.json     # Locked dependency versions
```

The repository also contains screenshots and deployment evidence from the course work. These files document AWS, API, database, frontend, and testing results and are retained as academic evidence rather than application dependencies.

## Running the Application

### Local development

Install the project dependencies and start the Angular development server:

```bash
npm install
npm start
```

Then open `http://localhost:4200/`.

### Production build

```bash
npm run build
```

The resulting Angular build can be prepared for static hosting such as Amazon S3.

### Docker

Build and run the application with Docker Compose:

```bash
docker network create lafs-net
docker compose up --build
```

The application is exposed on port `4200`.

> **Note:** The project uses an older Angular/Node toolchain because this is a course project built on the original application foundation. The Dockerfile now uses the Angular CLI 7.3.x line to match the project's Angular dependencies rather than the previously mismatched CLI 6 installation.

## Cloud Deployment Work

### Amazon S3

The Angular frontend was prepared as a static production build for S3 hosting. Deployment evidence is included in the repository screenshots and `docs/aws-deployment.md`.

### AWS Lambda

Lambda was explored as part of the serverless/API portion of the cloud migration. The repository documents the role of serverless components without committing credentials or private AWS configuration.

### CORS

The browser frontend and API can run on different origins. CORS configuration is therefore part of the integration layer and should be restricted to the origins and methods actually required by the application.

## Key Skills Demonstrated

- Full-stack application development
- Angular and TypeScript development
- REST API integration
- Node.js / Express concepts
- MongoDB integration
- Docker containerization
- Docker Compose orchestration
- AWS S3 deployment
- AWS Lambda/serverless concepts
- CORS configuration
- Build and dependency troubleshooting
- Cloud deployment troubleshooting
- Git and GitHub workflow
- Technical documentation
- Testing and quality assurance

## Documentation

- [`docs/project-overview.md`](docs/project-overview.md) — project purpose and technical context
- [`docs/cloud-architecture.md`](docs/cloud-architecture.md) — architecture and design considerations
- [`docs/aws-deployment.md`](docs/aws-deployment.md) — S3, Lambda, CORS, and deployment checklist
- [`docs/api-documentation.md`](docs/api-documentation.md) — API resources and integration notes
- [`docs/testing.md`](docs/testing.md) — testing approach and QA considerations
- [`docs/technical-presentation.md`](docs/technical-presentation.md) — presentation structure and talking points
- [`portfolio/portfolio-checklist.md`](portfolio/portfolio-checklist.md) — portfolio completion checklist
- [`portfolio/resume-project-summary.md`](portfolio/resume-project-summary.md) — resume-ready project summary

## Relationship to CS-465

CS-470 extends the full-stack foundation developed in CS-465. The earlier project established the application, API, database integration, and Angular administration experience. CS-470 adds the cloud, containerization, deployment, and infrastructure perspective.

**Related repository:** [rakim0112/CS465-Fullstack](https://github.com/rakim0112/CS465-Fullstack)

## Security and Repository Hygiene

No AWS access keys, database passwords, API secrets, or private `.env` files should be committed to this repository. Local secrets are excluded by `.gitignore`.

The repository's `.firebase/` cache is also ignored so local Firebase deployment artifacts do not become part of future commits.

## Future Improvements

For a production implementation, I would add:

- Automated CI/CD
- Infrastructure as code
- Automated unit, integration, and end-to-end testing
- Centralized logging and monitoring
- Least-privilege IAM policies
- Managed secret storage
- HTTPS and stronger security controls
- API validation and rate limiting
- Cost and scalability monitoring

## Academic Context

This repository is an academic portfolio artifact for CS-470. Course evidence is retained where it helps demonstrate the development and deployment process. Production credentials and unrelated generated files should not be added to source control.

---

**Author:** Rakim Spriggs  
**GitHub:** https://github.com/rakim0112
