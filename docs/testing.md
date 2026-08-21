# Testing and Quality Assurance

## Testing Approach

Testing for the project focused on verifying that individual application layers worked and that the components could communicate correctly. Troubleshooting was performed incrementally so that frontend, API, database, Docker, and cloud configuration problems could be isolated.

## Areas to Verify

- Angular application builds successfully.
- Frontend routes and components load correctly.
- API endpoints return the expected responses.
- Database operations succeed through the backend.
- Docker containers start with the expected configuration.
- Docker networking allows required services to communicate.
- CORS permits the intended frontend/API interaction.
- AWS-hosted frontend assets load correctly.
- Cloud/API integration works from the deployed application.
- No secrets or credentials are exposed in source control.

## Lessons From Troubleshooting

One of the most useful lessons was that a failure during a build does not necessarily mean the application code itself is incorrect. Version mismatches, missing packages, container configuration, environment variables, and deployment settings can all cause failures. Reading the complete error message and checking the environment before changing application logic makes debugging more efficient.

## Future QA Improvements

For a production version, I would add automated unit and integration tests, API contract tests, end-to-end browser tests, dependency/security scanning, CI checks, and deployment smoke tests.
