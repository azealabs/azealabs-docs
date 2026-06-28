# AZea Labs - Architecture

## 1. Architecture Overview

AZea Labs will be built as a connected ecosystem of independent products.

Each product should have a clear responsibility, its own codebase when needed, and a deployment strategy that allows it to grow independently.

The initial goal is not to create a complex enterprise architecture. The goal is to start simple, keep costs low, and design the ecosystem in a way that allows future growth.

Main products:

* AZea Labs Portfolio
* QA Labs
* QA Academy
* Future Projects

---

## 2. High-Level Ecosystem Architecture

Initial ecosystem structure:

```text
azealabs.com
│
├── Portfolio / Main Hub
│
├── labs.azealabs.com
│   └── QA Labs practice platform
│
├── academy.azealabs.com
│   └── Future QA Academy
│
├── api.azealabs.com
│   └── Future backend/API services
│
└── docs.azealabs.com
    └── Future public documentation
```

The portfolio will be the first product to build and deploy.

QA Labs will be the second product and will become the main technical platform.

QA Academy will be created later and will use QA Labs as its practice environment.

---

## 3. Architecture Principles

AZea Labs should follow these architecture principles:

* Start simple, but not improvised.
* Separate products by responsibility.
* Avoid unnecessary complexity at the beginning.
* Use standard technologies.
* Keep the system easy to move between hosting providers.
* Keep frontend, backend, and database separated.
* Use GitHub as the source of truth.
* Document important technical decisions.
* Prefer modular architecture before microservices.
* Design QA Labs to be automation-friendly.

---

## 4. Initial Product Architecture

### 4.1 Portfolio Architecture

The portfolio should be simple, fast, and easy to maintain.

Recommended approach:

```text
Static or mostly static website
```

Possible stack:

```text
Astro or Next.js
TypeScript
Tailwind CSS
Cloudflare Pages or Vercel
GitHub
```

Main responsibilities:

* Present the AZea Labs brand.
* Present Antonio Zea professionally.
* Link to projects.
* Link to QA Labs.
* Link to future QA Academy.
* Publish technical content.

The portfolio does not need a backend in the first version.

---

### 4.2 QA Labs Architecture

QA Labs will be the main practice platform for automation.

Initial approach:

```text
Frontend application + backend API + database
```

Suggested structure:

```text
QA Labs Frontend
│
└── QA Labs Backend API
    │
    └── PostgreSQL Database
```

Possible subdomains:

```text
labs.azealabs.com  -> QA Labs frontend
api.azealabs.com   -> QA Labs backend/API
```

Main responsibilities:

* Provide demo pages for automation practice.
* Provide API testing scenarios.
* Provide stable selectors.
* Provide test data.
* Support automation with Selenium, Cypress, Playwright, Robot Framework, and other tools.

---

### 4.3 QA Academy Architecture

QA Academy will be created later.

Initial approach:

```text
Educational website or learning platform
```

Possible subdomain:

```text
academy.azealabs.com
```

The academy should remain separate from QA Labs.

QA Academy will teach automation.

QA Labs will provide the practice environment.

---

## 5. Backend Architecture Direction

The backend should not start as microservices.

The recommended initial backend approach is:

```text
Modular monolith
```

This means the backend will start as one application, but internally organized into modules.

Possible backend modules:

```text
backend/
│
├── auth/
├── users/
├── playground/
├── api_lab/
├── test_data/
├── challenges/
├── reports/
└── shared/
```

This approach allows the project to stay simple while preparing for future growth.

If one module becomes too large in the future, it can be separated into its own service.

---

## 6. Why Not Microservices at the Beginning?

Microservices are powerful, but they add complexity.

Starting with microservices would require:

* Multiple deployments.
* Service-to-service communication.
* More monitoring.
* More logging.
* More DevOps work.
* More infrastructure cost.
* More complex debugging.
* More complex authentication between services.

For the first versions of AZea Labs and QA Labs, this is unnecessary.

The recommended strategy is:

```text
Start with a modular monolith.
Extract services later only when there is a real need.
```

---

## 7. Possible Future Microservices

If QA Labs grows, some modules could become independent services.

Possible future services:

```text
auth-service
users-service
playground-service
challenge-service
report-service
notification-service
academy-service
```

This should only happen when the project has enough complexity to justify it.

---

## 8. Frontend Architecture Direction

Frontend projects should use a component-based architecture.

Possible frontend structure:

```text
src/
│
├── components/
├── layouts/
├── pages/
├── features/
├── services/
├── styles/
├── data/
└── utils/
```

For QA Labs, features may be organized by testing scenario:

```text
features/
│
├── login-demo/
├── forms-demo/
├── tables-demo/
├── upload-demo/
├── dashboard-demo/
└── api-demo/
```

Each feature should be clear, testable, and easy to document.

---

## 9. Automation-Friendly Design

QA Labs should be designed for automation from the beginning.

Each important UI element should include stable selectors.

Example:

```html
<input
  id="username"
  name="username"
  data-testid="login-username"
  data-qa="login-username"
/>
```

Automation design rules:

* Use stable `data-testid` attributes.
* Avoid random IDs for important elements.
* Provide predictable test data.
* Add positive and negative scenarios.
* Document expected results.
* Make demo pages stable for learning.
* Add advanced dynamic behavior only in specific challenge pages.

QA Labs should include different difficulty levels:

```text
Basic mode      -> stable selectors and simple flows
Realistic mode  -> async behavior, loaders, dynamic data
Challenge mode  -> harder scenarios for advanced automation
```

---

## 10. Data Architecture

The first portfolio version does not need a database.

QA Labs will eventually need a database.

Recommended database:

```text
PostgreSQL
```

Possible providers:

```text
Neon
Supabase
Railway PostgreSQL
Render PostgreSQL
```

Initial database areas:

```text
users
roles
demo_data
products
orders
challenges
test_runs
reports
```

The database should be designed gradually. The first version does not need all tables.

---

## 11. API Architecture

The API should be designed using REST first.

Possible API areas:

```text
/auth
/users
/products
/orders
/playground
/challenges
/reports
```

Example endpoints:

```text
POST /auth/login
POST /auth/logout
GET /users
POST /users
PUT /users/{id}
DELETE /users/{id}
GET /products
POST /orders
```

The API should include OpenAPI/Swagger documentation.

This will help with:

* API testing.
* QA Academy lessons.
* Postman collections.
* Robot Framework API tests.
* Playwright API tests.

---

## 12. Deployment Architecture

Initial deployment strategy:

```text
GitHub
│
├── Portfolio
│   └── Cloudflare Pages or Vercel
│
├── QA Labs Frontend
│   └── Cloudflare Pages or Vercel
│
├── QA Labs Backend
│   └── Render or Railway
│
└── Database
    └── Neon or Supabase
```

The goal is to keep the first version affordable.

Initial hosting cost should be close to zero, except for the domain.

As the project grows, paid backend/database services may be added.

---

## 13. Repository Architecture

Initial repository strategy:

```text
azealabs/
│
├── azealabs-docs
├── portfolio
├── qalabs-web
├── qalabs-api
├── automation-examples
└── qa-academy
```

Recommended order:

1. `azealabs-docs`
2. `portfolio`
3. `qalabs-web`
4. `qalabs-api`
5. `automation-examples`
6. `qa-academy`

The first code repository should be:

```text
portfolio
```

---

## 14. Environment Strategy

Applications should use environment variables for configuration.

Examples:

```text
API_BASE_URL
DATABASE_URL
JWT_SECRET
APP_ENV
PUBLIC_SITE_URL
```

No secrets should be committed to GitHub.

Each project should include:

```text
.env.example
```

This file documents required environment variables without exposing real secrets.

---

## 15. Portability Strategy

AZea Labs should avoid vendor lock-in when possible.

Rules:

* Keep code in GitHub.
* Use standard frameworks.
* Use PostgreSQL instead of a provider-specific database.
* Use Docker for backend services when possible.
* Keep environment variables separated from code.
* Avoid depending too heavily on proprietary platform features at the beginning.

This will allow the project to move from one provider to another if needed.

---

## 16. Future Architecture Direction

Future architecture may include:

* Shared design system.
* Shared authentication.
* API gateway.
* Background jobs.
* Monitoring.
* Logging.
* Analytics.
* Microservices.
* Mobile applications.
* Tablet applications.
* Public documentation portal.

These should be added only when the project needs them.

---

## 17. Current Architecture Decision

The initial architecture decision is:

```text
Use a simple, modular, low-cost architecture.
Start with the portfolio.
Build QA Labs as a separated product.
Use a modular monolith for the backend.
Avoid microservices at the beginning.
Prepare the system for future growth.
```

This approach supports the main philosophy of AZea Labs:

```text
Start simple, but not improvised.
```

