# Cloud-Based Full-Stack Application

**Angular · TypeScript · Node.js · Express · MongoDB · Docker · AWS**

A cloud-focused extension of a full-stack web application. The project explores the steps required to move an application toward a cloud deployment model, including containerization, production builds, AWS services, serverless components, API integration, and troubleshooting across development environments.

## Project Highlights

- Angular frontend development
- Node.js / Express API foundation
- MongoDB integration
- Docker containerization
- Docker Compose orchestration
- Production build preparation
- Amazon S3 static-hosting workflow
- AWS Lambda/serverless integration work
- CORS configuration and cross-origin API considerations
- Build and dependency troubleshooting
- Technical documentation and deployment planning

## Architecture

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

Cloud components:
Angular production build --> Amazon S3
Serverless/API work ------> AWS Lambda
Browser/API integration --> CORS
Local environment -------> Docker / Docker Compose
```

## Technology Stack

| Area | Technology |
|---|---|
| Frontend | Angular 7 / TypeScript |
| UI | Angular Material / Bootstrap Sass / Font Awesome |
| Backend | Node.js / Express |
| Database | MongoDB |
| Cloud | Amazon Web Services |
| Static Hosting | Amazon S3 |
| Serverless | AWS Lambda |
| Containers | Docker / Docker Compose |
| Integration | REST / CORS |
| Version Control | Git / GitHub |

## What I Built and Learned

The project builds on the full-stack foundation from CS-465 and adds a cloud and deployment perspective. I worked through containerizing the application, orchestrating local services with Docker Compose, preparing Angular production builds, working with Amazon S3, exploring Lambda for serverless/API functionality, and troubleshooting dependency and environment issues.

The project also reinforced the importance of separating application concerns, documenting deployment assumptions, keeping credentials out of source control, and treating cloud deployment as more than simply moving an application to a different server.

## Documentation

The repository contains supporting documentation covering architecture, AWS deployment work, API integration, testing, and technical presentation material.

## Relationship to Travlr

This project extends the application foundation developed in the Travlr full-stack project. CS-465 established the frontend, API, database, CRUD, and authentication work; this project adds containerization, cloud services, deployment preparation, and infrastructure considerations.

Related project: https://github.com/rakim0112/CS465-Fullstack

## Security

No AWS credentials, database passwords, API secrets, or private `.env` files should be committed to this repository. Deployment credentials should remain in local configuration or an appropriate secret-management system.

## Academic Context

Originally developed as part of SNHU's CS-470 Full Stack Development II coursework. The repository is presented as a technical portfolio project with emphasis on cloud, deployment, containerization, and troubleshooting skills.

## Author

**Rakim Spriggs**  
B.S. Computer Science — Southern New Hampshire University  
Expected December 2026
