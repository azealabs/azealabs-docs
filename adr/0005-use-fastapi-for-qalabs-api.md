# ADR 0005 - Use FastAPI for QA Labs API

## Status

Accepted

## Date

2026-06-28

## Context

QA Labs will include API testing practice as part of its MVP and future roadmap.

The platform needs a backend API that can support:

```text
Health check endpoint
Authentication-like scenarios
Users CRUD endpoints
Validation examples
Status code testing
Payload testing
Error response testing
OpenAPI documentation
Future integration with the QA Labs frontend
```

The API should be easy to develop, easy to document, and useful for automation engineers practicing API testing.

The backend should also support future expansion without introducing unnecessary complexity too early.

## Decision

QA Labs API will use:

```text
Python
FastAPI
Pydantic
```

The initial repository will be:

```text
qalabs-api
```

The planned public URL will be:

```text
https://api.azealabs.com
```

## Considered Options

### Option 1 - Node.js with Express

Express is simple, popular, and flexible.

However, it requires more manual setup for validation, API documentation, structure, and typing unless additional libraries are added.

### Option 2 - NestJS

NestJS is powerful and structured.

It is a good choice for large backend applications, but it introduces more complexity than needed for the first QA Labs API MVP.

### Option 3 - Django REST Framework

Django REST Framework is mature and powerful.

It works well for full backend systems, but it may be heavier than necessary for the first QA Labs API MVP.

### Option 4 - FastAPI

FastAPI provides a strong balance between simplicity, modern Python development, validation, automatic documentation, and API-first design.

It is well suited for building endpoints that automation engineers can test and understand.

## Rationale

FastAPI is selected because it is practical, modern, and documentation-friendly.

It provides:

```text
Automatic OpenAPI documentation
Built-in request and response validation
Strong Pydantic integration
Clean endpoint definitions
Good Python developer experience
Support for async endpoints
Simple local development
Good fit for API testing practice
```

FastAPI is also a good learning tool because it makes API behavior visible through generated documentation.

This supports the goal of QA Labs: helping automation engineers practice with realistic and understandable systems.

## Consequences

### Positive Consequences

```text
The API will be easy to document
OpenAPI documentation will be available automatically
Request and response models can be clearly defined
API testing scenarios will be easier to create
The backend will be approachable for learning and teaching
Python aligns well with many QA automation workflows
```

### Negative Consequences

```text
The project will require backend deployment planning
The team must manage Python dependencies carefully
Production configuration will need environment variables and security considerations
Async patterns may add learning overhead
```

## Initial API Scope

The MVP API should include:

```text
GET /health
POST /auth/login
POST /auth/logout
GET /users
POST /users
GET /users/{id}
PUT /users/{id}
DELETE /users/{id}
```

The API should return predictable data and clear error responses.

## Implementation Notes

The first version should start as a modular monolith.

Do not introduce microservices.

Recommended initial structure:

```text
qalabs-api/
├── app/
│   ├── main.py
│   ├── api/
│   ├── models/
│   ├── schemas/
│   ├── services/
│   └── core/
├── tests/
├── Dockerfile
├── .env.example
└── README.md
```

The API should include:

```text
Clear endpoint names
Consistent response formats
Predictable sample data
Validation errors
OpenAPI documentation
Health endpoint
Basic automated tests in the future
```

## Related Documents

```text
docs/04-architecture.md
docs/05-tech-stack.md
docs/08-backlog.md
docs/09-qalabs-mvp-scope.md
```

## Decision Summary

QA Labs API will use **FastAPI with Python and Pydantic** because it provides a clean, modern, and well-documented backend foundation for API testing practice.

