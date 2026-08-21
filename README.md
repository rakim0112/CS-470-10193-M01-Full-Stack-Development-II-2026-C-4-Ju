# CS-470 Full Stack Development II

## Cloud-Based Full-Stack Application Portfolio

**Student:** Rakim Spriggs  
**Course:** CS-470 Full Stack Development II  
**Term:** 2026 C-4  
**Program:** B.S. Computer Science, Southern New Hampshire University

---

## Project Overview

This repository documents my CS-470 work building and preparing a full-stack application for cloud deployment. The project builds on the application developed in CS-465 Full Stack Development I and focuses on taking a working full-stack solution into a cloud environment.

The project gave me practical experience with containerization, multi-container development, REST APIs, MongoDB, Angular, Node.js/Express, AWS services, deployment configuration, and troubleshooting across different environments.

The goal was not only to make the application work locally, but to understand what is required to move an application toward a production-style cloud architecture.

## Technology Stack

- **Frontend:** Angular
- **Backend:** Node.js and Express
- **Database:** MongoDB
- **Cloud:** Amazon Web Services (AWS)
- **Storage/Hosting:** Amazon S3
- **Serverless:** AWS Lambda
- **API:** REST
- **Security/Integration:** CORS configuration
- **Containerization:** Docker and Docker Compose
- **Version Control:** Git and GitHub

## Architecture

At a high level, the application separates the client interface, server-side API, and database responsibilities. Docker was used to create repeatable development environments, while AWS services were introduced as part of the cloud migration and deployment process.

```text
Angular Client
      |
      v
REST API / Node.js + Express
      |
      v
   MongoDB

Cloud deployment components:
Angular build -> Amazon S3
API/serverless components -> AWS services
Cross-origin communication -> CORS
```

See [`docs/cloud-architecture.md`](docs/cloud-architecture.md) for additional detail.

## Key CS-470 Work

### Containerization

I used Docker to package application components and Docker Compose to coordinate multiple services during development. This helped me understand how application components communicate within a consistent environment instead of depending entirely on software installed directly on the host machine.

### Cloud Deployment

I worked with AWS S3 as part of deploying the Angular frontend and worked through the build and environment issues required to produce a deployable frontend artifact. I also worked with AWS Lambda and CORS as part of the cloud/API portion of the project.

### Troubleshooting

A significant part of the project involved diagnosing compatibility and build problems. I worked through Node.js and Angular tooling issues, container configuration, dependency installation, build commands, and cloud configuration. These problems reinforced the importance of checking versions, reading error messages carefully, and testing one layer of the application at a time.

## Relationship to CS-465

CS-470 continues the full-stack development work from CS-465. The earlier project established the application structure, database integration, API, and Angular administration interface. CS-470 focuses on extending that foundation into a cloud-oriented architecture.

**Related project:** [CS465-Fullstack](https://github.com/rakim0112/CS465-Fullstack)

## Skills Demonstrated

- Full-stack web development
- REST API development
- Angular application development
- Node.js/Express backend development
- MongoDB integration
- Docker containerization
- Docker Compose orchestration
- AWS cloud services
- S3 deployment
- Serverless concepts with AWS Lambda
- CORS configuration
- Git/GitHub version control
- Debugging and environment troubleshooting
- Technical documentation

## Portfolio Value

This project demonstrates my ability to move beyond writing individual application features and think about how a complete software system is built, configured, deployed, and maintained. It is especially relevant to entry-level **full-stack developer, cloud developer, backend developer, and software developer** positions.

The project also complements my other computer science portfolio work in client/server development, software testing, UI/UX, graphics, and full-stack development.

## Future Improvements

If this application were continued as a production project, I would add automated CI/CD, infrastructure-as-code, centralized logging and monitoring, stronger environment and secret management, automated security testing, more comprehensive integration tests, and additional AWS services where they provide measurable value.

## Academic Context

This repository is an academic portfolio artifact for CS-470. Course-specific work is documented for educational and portfolio purposes. Sensitive credentials, API keys, passwords, and other private configuration values should never be committed to this repository.

---

**Author:** Rakim Spriggs  
**GitHub:** https://github.com/rakim0112
