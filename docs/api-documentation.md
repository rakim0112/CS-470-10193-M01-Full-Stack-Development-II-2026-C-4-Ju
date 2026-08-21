# API Documentation

## Overview

The application uses a REST-style API to separate frontend responsibilities from backend application logic. The API is responsible for accessing and modifying application data through the backend and database layers.

## Core Resources

The CS-465 foundation for this application includes trip resources and the following API pattern:

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/trips` | Retrieve available trips |
| GET | `/api/trips/:tripCode` | Retrieve a specific trip by trip code |

The exact deployed endpoint depends on the cloud configuration used for the CS-470 environment.

## Integration

The Angular client communicates with the API over HTTP. When the frontend and API use different origins, CORS must permit only the required frontend origin and HTTP methods.

## Production Improvements

For a production API, I would add authentication and authorization where required, request validation, centralized error handling, rate limiting, structured logging, automated API tests, HTTPS, secure environment configuration, and monitoring.
