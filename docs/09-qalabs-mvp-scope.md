# QA Labs - MVP Scope

## 1. Document Overview

This document defines the initial MVP scope for **QA Labs**, the first major product under the AZea Labs ecosystem.

QA Labs will be a practice platform for QA automation engineers. It will provide realistic web pages, API endpoints, testing scenarios, stable selectors, and documentation designed for automation practice.

The goal of this document is to define what will be included in the first version of QA Labs, what will not be included yet, and what success looks like for the MVP.

---

## 2. Product Summary

### Product Name

```text
QA Labs
```

### Product Type

```text
QA automation practice platform
```

### Future URL

```text
https://labs.azealabs.com
```

### Parent Ecosystem

```text
AZea Labs
```

### Main Purpose

QA Labs exists to provide a realistic and structured environment where automation engineers can practice UI automation, API testing, test design, selector strategies, and framework implementation.

The platform will be intentionally designed for automation practice, unlike generic demo websites that are often too simple, outdated, or poorly documented.

---

## 3. Product Vision

QA Labs will become a practical training environment for automation engineers.

It will include:

```text
Web UI demo pages
API endpoints
Stable selectors
Testing scenarios
Documentation
Automation examples
Difficulty levels
Realistic workflows
```

The long-term vision is for QA Labs to support:

```text
Self-practice
Portfolio projects
Automation tutorials
Future QA Academy lessons
Framework comparison examples
Technical documentation
Real-world testing exercises
```

---

## 4. MVP Objective

The MVP objective is to release the first public version of QA Labs with enough functionality to support basic automation practice.

The MVP should allow a user to:

```text
Visit labs.azealabs.com
Open demo pages
Understand what each page is for
Automate basic UI scenarios
Use stable selectors
Practice API testing against simple endpoints
Read documentation for each scenario
```

The MVP does not need to be large. It needs to be clear, stable, documented, and useful.

---

## 5. Target Users

### Primary Users

```text
QA automation engineers
Manual testers learning automation
QA engineers building portfolio projects
Automation students
Developers interested in testability
```

### Secondary Users

```text
Recruiters reviewing portfolio work
Technical interviewers
Future QA Academy students
Automation instructors
```

---

## 6. MVP Goals

The MVP should achieve these goals:

```text
Provide a public automation practice platform
Show professional product thinking
Demonstrate testability-first design
Support UI automation practice
Support basic API testing practice
Use stable selectors
Provide scenario documentation
Prepare the foundation for automation examples
Prepare the foundation for QA Academy
```

---

## 7. MVP Non-Goals

The MVP will not include everything.

The following items are intentionally out of scope for the first version:

```text
User registration
Real user accounts
Payments
Course platform functionality
Complex dashboards
Advanced role permissions
Production-grade authentication
Real database-heavy workflows
Multi-tenant architecture
Admin portal
Mobile app
Full academy content
Video lessons
Advanced analytics
Microservices
Kubernetes
Complex cloud infrastructure
```

These can be considered in future phases after the MVP is stable.

---

## 8. Core MVP Scope

The first version of QA Labs should include:

```text
Public landing page
Demo pages for UI automation
Basic API endpoints
Stable data-testid selectors
Scenario documentation
Basic responsive design
Clear navigation
Simple design system
Deployment to labs.azealabs.com
```

---

## 9. Initial Demo Pages

The MVP should include a small but useful set of demo pages.

### 9.1 Login Demo

Purpose:

```text
Practice login automation, validation messages, and authentication-like flows.
```

Initial scenarios:

```text
Successful login with valid credentials
Failed login with invalid credentials
Empty username validation
Empty password validation
Locked user message
Logout flow
```

Recommended selectors:

```text
data-testid="login-username-input"
data-testid="login-password-input"
data-testid="login-submit-button"
data-testid="login-error-message"
data-testid="logout-button"
```

---

### 9.2 Forms Demo

Purpose:

```text
Practice form filling, validation, dropdowns, checkboxes, radio buttons, and submit behavior.
```

Initial scenarios:

```text
Submit valid form
Submit form with required fields missing
Validate email format
Select dropdown option
Check and uncheck checkbox
Select radio option
Reset form
```

Recommended selectors:

```text
data-testid="form-name-input"
data-testid="form-email-input"
data-testid="form-role-select"
data-testid="form-terms-checkbox"
data-testid="form-submit-button"
data-testid="form-reset-button"
data-testid="form-success-message"
data-testid="form-error-message"
```

---

### 9.3 Tables Demo

Purpose:

```text
Practice table validation, search, filtering, sorting, pagination, and row actions.
```

Initial scenarios:

```text
Validate table rows
Search by text
Filter by status
Sort by column
Navigate pagination
Open row details
Delete row confirmation
```

Recommended selectors:

```text
data-testid="table-search-input"
data-testid="table-status-filter"
data-testid="table-users"
data-testid="table-row-{id}"
data-testid="table-sort-name"
data-testid="table-pagination-next"
data-testid="table-pagination-previous"
```

---

### 9.4 Upload Demo

Purpose:

```text
Practice file upload automation.
```

Initial scenarios:

```text
Upload valid file
Reject invalid file type
Reject oversized file
Show uploaded file name
Clear selected file
```

Recommended selectors:

```text
data-testid="upload-file-input"
data-testid="upload-submit-button"
data-testid="upload-file-name"
data-testid="upload-success-message"
data-testid="upload-error-message"
```

---

### 9.5 Download Demo

Purpose:

```text
Practice file download automation.
```

Initial scenarios:

```text
Download CSV file
Download PDF file
Validate download trigger
Validate file name
```

Recommended selectors:

```text
data-testid="download-csv-button"
data-testid="download-pdf-button"
data-testid="download-status-message"
```

---

### 9.6 Dashboard Demo

Purpose:

```text
Practice dashboard validation, cards, charts placeholders, and dynamic UI states.
```

Initial scenarios:

```text
Validate summary cards
Filter dashboard data
Show loading state
Show empty state
Show error state
Refresh dashboard
```

Recommended selectors:

```text
data-testid="dashboard-total-users-card"
data-testid="dashboard-active-users-card"
data-testid="dashboard-filter-select"
data-testid="dashboard-refresh-button"
data-testid="dashboard-loading-state"
data-testid="dashboard-empty-state"
data-testid="dashboard-error-state"
```

---

## 10. Initial API Scope

The MVP should include a simple API that supports API testing practice.

### Base API URL

Future target:

```text
https://api.azealabs.com
```

During local development:

```text
http://localhost:8000
```

---

### 10.1 Health Check

```text
GET /health
```

Purpose:

```text
Validate that the API is running.
```

Expected response:

```json
{
  "status": "ok",
  "service": "qa-labs-api"
}
```

---

### 10.2 Login

```text
POST /auth/login
```

Purpose:

```text
Practice authentication-style API testing.
```

Example request:

```json
{
  "username": "standard_user",
  "password": "secret"
}
```

Example success response:

```json
{
  "token": "sample-token",
  "user": {
    "id": 1,
    "username": "standard_user",
    "role": "tester"
  }
}
```

Example failure response:

```json
{
  "error": "Invalid username or password"
}
```

---

### 10.3 Logout

```text
POST /auth/logout
```

Purpose:

```text
Practice logout endpoint validation.
```

Example response:

```json
{
  "message": "Logged out successfully"
}
```

---

### 10.4 Users

```text
GET /users
POST /users
GET /users/{id}
PUT /users/{id}
DELETE /users/{id}
```

Purpose:

```text
Practice CRUD API testing.
```

Example user object:

```json
{
  "id": 1,
  "name": "Ana López",
  "email": "ana@example.com",
  "role": "QA Engineer",
  "status": "active"
}
```

---

## 11. Automation-Friendly Design Rules

QA Labs must be designed with automation in mind.

### 11.1 Stable Selectors

All important interactive elements should include stable selectors.

Preferred selector:

```text
data-testid
```

Example:

```html
<button data-testid="login-submit-button">Login</button>
```

Avoid relying on:

```text
CSS classes
Auto-generated IDs
Visual text only
DOM position
Complex XPath
```

---

### 11.2 Predictable Test Data

The MVP should include predictable test data.

Examples:

```text
standard_user
locked_user
invalid_user
admin_user
```

Sample login data:

```text
standard_user / secret
locked_user / secret
```

---

### 11.3 Clear UI States

Pages should include states that are useful for test automation.

Examples:

```text
Success state
Error state
Loading state
Empty state
Validation state
Disabled state
Confirmation state
```

---

### 11.4 Scenario Documentation

Every demo page should have a documentation section that explains:

```text
Purpose of the page
Available scenarios
Recommended selectors
Valid test data
Expected results
Common automation checks
```

---

## 12. Initial Framework Support

QA Labs should be usable with:

```text
Selenium WebDriver
Cypress
Playwright
Robot Framework
Postman
REST Assured
Python requests
```

The MVP does not need to include examples for all frameworks immediately, but the platform should be designed so that examples can be added later.

---

## 13. Future Automation Examples Repository

A future repository should be created:

```text
automation-examples
```

Suggested structure:

```text
automation-examples/
├── selenium/
├── cypress/
├── playwright/
├── robot-framework/
├── postman/
└── README.md
```

Initial example scenarios:

```text
Login with valid user
Login with invalid user
Submit form successfully
Search table data
Call health endpoint
Create user through API
```

---

## 14. Recommended Technical Stack

### Frontend

```text
Next.js
TypeScript
Tailwind CSS
```

### Backend

```text
Python
FastAPI
Pydantic
```

### Database

```text
PostgreSQL
```

### Local Development

```text
Docker
Docker Compose
```

### Deployment

Possible options:

```text
Cloudflare Pages for frontend
Render, Railway, Fly.io, or similar for backend
Neon or Supabase for PostgreSQL
Cloudflare DNS for subdomains
```

---

## 15. Initial Architecture Direction

The first version should use a simple architecture.

Recommended approach:

```text
Frontend application
Backend API
PostgreSQL database
Shared documentation
```

Backend architecture should start as a modular monolith.

Do not start with microservices.

Reason:

```text
The MVP needs clarity, speed, and maintainability.
Microservices would add unnecessary complexity too early.
```

---

## 16. Repositories

Suggested repositories:

```text
qalabs-web
qalabs-api
automation-examples
```

Repository purposes:

```text
qalabs-web:
Frontend application for labs.azealabs.com

qalabs-api:
Backend API for api.azealabs.com

automation-examples:
Automation tests written against QA Labs
```

---

## 17. Subdomains

Planned subdomains:

```text
labs.azealabs.com
api.azealabs.com
docs.azealabs.com
```

MVP priority:

```text
labs.azealabs.com
api.azealabs.com
```

---

## 18. MVP Success Criteria

The MVP is successful when:

```text
labs.azealabs.com is publicly available
The frontend has at least 3 demo pages
The API has a working health endpoint
The API has basic auth and users endpoints
Demo pages include stable data-testid selectors
Each demo page includes scenario documentation
At least one UI flow can be automated
At least one API flow can be automated
The project is documented in GitHub
The platform is stable enough for future automation examples
```

---

## 19. Suggested MVP Milestones

### Milestone 1 - Planning

```text
Define MVP scope
Define demo pages
Define selectors
Define test data
Define API endpoints
Define repository structure
```

### Milestone 2 - Frontend Foundation

```text
Create qalabs-web repository
Initialize Next.js project
Add Tailwind CSS
Create layout and navigation
Create QA Labs landing page
Deploy frontend to labs.azealabs.com
```

### Milestone 3 - UI Demo Pages

```text
Create Login Demo
Create Forms Demo
Create Tables Demo
Add documentation section per page
Add stable selectors
```

### Milestone 4 - API Foundation

```text
Create qalabs-api repository
Initialize FastAPI project
Create health endpoint
Create auth endpoints
Create users endpoints
Add OpenAPI documentation
Deploy API to api.azealabs.com
```

### Milestone 5 - Automation Examples

```text
Create first Playwright example
Create first Selenium example
Create first Robot Framework example
Create first API test example
Document how to run examples
```

---

## 20. Risks and Mitigations

### Risk: Scope grows too much

Mitigation:

```text
Keep MVP small.
Start with 3 UI demo pages and a simple API.
Move advanced ideas to future backlog.
```

### Risk: Platform becomes too academic

Mitigation:

```text
Use realistic scenarios and real automation problems.
Include validation, loading states, filters, tables, APIs, and test data.
```

### Risk: Selectors become inconsistent

Mitigation:

```text
Define data-testid conventions early.
Review every demo page before release.
```

### Risk: Too much infrastructure too early

Mitigation:

```text
Start simple.
Avoid Kubernetes, microservices, and complex cloud architecture.
```

---

## 21. Open Questions

These questions should be answered before development starts:

```text
Should QA Labs start with frontend only or frontend + API together?
Should the first frontend use mock data or connect to the API immediately?
Which 3 demo pages should be included first?
Should authentication be simulated or API-driven in the MVP?
Which deployment provider should be used for the backend?
Should automation examples live in a separate repository from the beginning?
```

---

## 22. Recommended First MVP Version

The recommended first MVP version should include:

```text
QA Labs landing page
Login Demo
Forms Demo
Tables Demo
Health API endpoint
Basic auth API endpoint
Basic users API endpoint
Scenario documentation
Stable selectors
Deployment to labs.azealabs.com
```

This is enough to make QA Labs useful without making the first version too large.

---

## 23. Immediate Next Tasks

The next tasks after approving this MVP scope are:

```text
1. Review and refine this MVP scope.
2. Create ADR for using Next.js for QA Labs frontend.
3. Create ADR for using FastAPI for QA Labs API.
4. Create ADR for using PostgreSQL.
5. Create `qalabs-web` repository.
6. Initialize frontend project.
7. Deploy initial QA Labs landing page to `labs.azealabs.com`.
8. Create `qalabs-api` repository.
9. Initialize API project.
10. Deploy health endpoint to `api.azealabs.com`.
```

---

## 24. Completion Criteria for This Document

This document is complete when:

```text
The MVP scope is clear
Initial demo pages are defined
Initial API endpoints are defined
Automation design rules are documented
Success criteria are defined
Next tasks are clear
```

---

## 25. Guiding Principle

QA Labs should be built with this principle:

```text
Design for automation from the beginning.
Keep the MVP small.
Make every feature useful for real testing practice.
Document everything clearly.
```
