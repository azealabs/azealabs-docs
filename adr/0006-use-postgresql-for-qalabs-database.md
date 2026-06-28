# ADR 0006 - Use PostgreSQL for QA Labs Database

## Status

Accepted

## Date

2026-06-28

## Context

QA Labs will eventually need persistent data for API testing, UI scenarios, users, roles, tables, filters, dashboards, and future learning exercises.

The first MVP may start with simple or seeded data, but the long-term product should use a database that supports realistic backend development and professional data modeling.

The database should support:

```text
Users
Roles
Demo records
Form submissions
Table data
Scenario data
API testing examples
Future dashboard data
Future academy integration
```

The selected database should be reliable, widely used, and useful for learning professional application development.

## Decision

QA Labs will use:

```text
PostgreSQL
```

For local development, PostgreSQL should run through:

```text
Docker
Docker Compose
```

For hosted environments, possible providers include:

```text
Neon
Supabase
Railway
Render
Other managed PostgreSQL providers
```

## Considered Options

### Option 1 - SQLite

SQLite is simple and excellent for local development.

However, QA Labs is intended to grow into a public platform with API scenarios, persistent data, and realistic workflows.

SQLite may be useful for early experiments, but it is not the preferred long-term database for QA Labs.

### Option 2 - MySQL

MySQL is mature and widely used.

It would work for the project, but PostgreSQL provides stronger alignment with modern backend development, advanced data features, and many managed cloud options.

### Option 3 - MongoDB

MongoDB is flexible and document-oriented.

However, QA Labs will benefit from relational modeling for users, roles, records, tables, statuses, and structured API examples.

A relational database is a better fit for the initial product direction.

### Option 4 - PostgreSQL

PostgreSQL is reliable, professional, widely used, and suitable for structured application data.

It supports relational modeling, constraints, indexing, JSON fields if needed, and strong compatibility with modern backend tools.

## Rationale

PostgreSQL is selected because QA Labs should be built with realistic professional architecture.

It provides:

```text
Relational data modeling
Strong data integrity
Good support for constraints
Good support for indexing
Compatibility with FastAPI ecosystem
Managed hosting options
Strong long-term scalability
Professional learning value
```

Using PostgreSQL also supports the goal of learning better software architecture and backend design.

## Consequences

### Positive Consequences

```text
The project will use a professional database system
Data modeling can be realistic
API scenarios can use persistent data
The database can support future growth
The stack aligns with modern backend development
The project can support more realistic automation scenarios
```

### Negative Consequences

```text
PostgreSQL requires more setup than mock data or SQLite
Local development will need Docker or a local PostgreSQL installation
Database migrations will need to be managed
Environment configuration will be required
```

## Implementation Notes

The MVP should not start with complex database design.

Initial database scope can include:

```text
users
roles
demo_records
form_submissions
```

The first version may use seeded data.

Recommended future tooling:

```text
SQLAlchemy or SQLModel
Alembic for migrations
Pydantic schemas for API validation
Docker Compose for local database
```

The project should include:

```text
.env.example
Database connection configuration
Migration strategy
Seed data strategy
Basic database documentation
```

## Initial Data Model Direction

Possible initial entities:

```text
User
Role
DemoRecord
FormSubmission
```

Possible future entities:

```text
Scenario
TestDataSet
DashboardMetric
UploadedFile
AuditLog
```

The database model should remain simple until the MVP requirements are clearer.

## Related Documents

```text
docs/04-architecture.md
docs/05-tech-stack.md
docs/08-backlog.md
docs/09-qalabs-mvp-scope.md
```

## Decision Summary

QA Labs will use **PostgreSQL** because it provides a reliable, professional, and scalable relational database foundation for realistic API and UI automation practice scenarios.

