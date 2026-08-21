# Cloud Architecture

## Architecture Summary

The application follows a separated frontend, API, and database design. The cloud portion introduces AWS services around the application while Docker provides a consistent development environment.

```text
User
  |
  v
Angular Frontend
  |
  | HTTP/REST
  v
Node.js + Express API
  |
  v
MongoDB

AWS deployment/support:
Angular production build -> Amazon S3
Serverless/API work -> AWS Lambda
Browser/API integration -> CORS
```

## Design Considerations

- Separate presentation, application logic, and data responsibilities.
- Use REST endpoints to keep frontend/backend responsibilities distinct.
- Use environment-specific configuration instead of hard-coding secrets.
- Use CORS only for the origins that need to communicate with the API.
- Keep credentials and private configuration outside source control.
- Test cloud components independently before integrating them.

## Production Considerations

A production implementation should add monitoring, centralized logging, automated deployment, least-privilege IAM policies, secure secret management, HTTPS, automated testing, and infrastructure-as-code. The architecture should also be reviewed for cost, availability, scalability, and security before being used for a real customer workload.
