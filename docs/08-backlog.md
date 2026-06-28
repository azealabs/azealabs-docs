# AZea Labs - Initial Backlog

## 1. Backlog Overview

This document defines the initial backlog for the AZea Labs ecosystem.

The backlog is organized by epics, products, and phases.

The goal is to keep the work clear, incremental, and aligned with the AZea Labs roadmap.

---

## 2. Current Focus

Current phase:

```text
Phase 1 - Portfolio MVP
```

Current objective:

```text
Improve the first public version of the AZea Labs Portfolio and prepare the project for QA Labs planning.
```

Next product to build:

```text
AZea Labs Portfolio
```

Main deployment target:

```text
azealabs.com
```

---

## 3. Epic 1 - Foundation and Documentation

### Goal

Create the initial documentation base for the ecosystem.

### Status

In progress.

### Tasks

* [x] Buy main domain: `azealabs.com`
* [x] Create GitHub organization: `azealabs`
* [x] Create documentation repository: `azealabs-docs`
* [x] Create Master Plan document
* [x] Create Vision document
* [x] Create Products document
* [x] Create Roadmap document
* [x] Create Architecture document
* [x] Create Tech Stack document
* [x] Create Domain Strategy document
* [x] Create GitHub Strategy document
* [x] Create Initial Backlog document
* [x] Create first ADR documents
* [ ] Review and refine documentation

### Completion Criteria

This epic is complete when the initial documentation is ready and the portfolio repository can be created with a clear direction.

---

## 4. Epic 2 - Branding Foundation

### Goal

Define the initial identity of AZea Labs.

### Tasks

* [x] Select main brand name: AZea Labs
* [x] Buy matching domain: `azealabs.com`
* [x] Define brand personality
* [x] Define initial color direction
* [x] Define typography direction
* [ ] Define visual style references
* [x] Create temporary logo or wordmark
* [x] Define portfolio visual style
* [ ] Define QA Labs visual style
* [ ] Define academy visual style

### Notes

The final visual identity does not need to be perfect before development starts.

The first version can use a clean, professional style and evolve later.

---

## 5. Epic 3 - Portfolio Planning

### Goal

Prepare the first version of the AZea Labs Portfolio.

### Tasks

* [x] Define portfolio sections
* [x] Define homepage content
* [x] Define About content
* [x] Define Projects content
* [x] Define QA Labs teaser content
* [x] Define contact information
* [x] Define GitHub and LinkedIn links
* [x] Define initial English copy
* [x] Define SEO metadata
* [x] Define first portfolio wireframe

### Initial Portfolio Sections

```text
Home
About
Projects
QA Labs
Future Academy
Blog Preview
Contact
```

### Completion Criteria

This epic is complete when the first portfolio structure and content are ready to be implemented.

---

## 6. Epic 4 - Portfolio Development

### Goal

Build and deploy the first version of `azealabs.com`.

### Tasks

* [x] Create `portfolio` repository
* [x] Initialize Astro project
* [x] Add TypeScript
* [x] Add Tailwind CSS
* [x] Create base layout
* [x] Create navigation
* [x] Create homepage hero section
* [x] Create About section
* [x] Create Projects section
* [x] Create QA Labs teaser section
* [x] Create Future Academy teaser section
* [x] Create Contact section
* [x] Add responsive styles
* [x] Add basic SEO metadata
* [ ] Add README
* [x] Deploy to Cloudflare Pages
* [x] Connect `azealabs.com`
* [x] Connect `www.azealabs.com`
* [x] Validate `www.azealabs.com` HTTPS
* [x] Create initial AZea Labs landing page
* [x] Validate HTTPS
* [ ] Test on desktop and mobile
* [ ] Add portfolio README
* [ ] Add favicon
* [ ] Add Open Graph metadata
* [ ] Add social preview image
* [ ] Add 404 page
* [ ] Configure canonical domain redirect
* [ ] Verify contact email works
* [ ] Add LinkedIn link
* [ ] Add first project details page

### Completion Criteria

This epic is complete when `https://azealabs.com` is publicly available with the first version of the portfolio.

---

## 7. Epic 5 - QA Labs Planning

### Goal

Define the first version of QA Labs before building it.

### Tasks

* [ ] Define QA Labs MVP scope
* [ ] Define first demo pages
* [ ] Define automation-friendly UI rules
* [ ] Define test scenario format
* [ ] Define page documentation format
* [ ] Define difficulty levels
* [ ] Define data-testid conventions
* [ ] Define first API scenarios
* [ ] Define future automation examples structure

### Initial QA Labs Demo Pages

```text
Login Demo
Forms Demo
Tables Demo
Upload Demo
Download Demo
Dashboard Demo
Basic API Demo
```

### Completion Criteria

This epic is complete when QA Labs MVP is clearly specified and ready for development.

---

## 8. Epic 6 - QA Labs Frontend MVP

### Goal

Build the first QA Labs frontend.

### Tasks

* [ ] Create `qalabs-web` repository
* [ ] Initialize Next.js project
* [ ] Add TypeScript
* [ ] Add Tailwind CSS
* [ ] Create QA Labs landing page
* [ ] Create Login Demo page
* [ ] Create Forms Demo page
* [ ] Create Tables Demo page
* [ ] Add stable selectors
* [ ] Add basic documentation per page
* [ ] Deploy to `labs.azealabs.com`

### Completion Criteria

This epic is complete when the first QA Labs demo pages are publicly available and can be automated.

---

## 9. Epic 7 - QA Labs API MVP

### Goal

Create the first backend API for QA Labs.

### Tasks

* [ ] Create `qalabs-api` repository
* [ ] Initialize FastAPI project
* [ ] Add project structure
* [ ] Add health check endpoint
* [ ] Add basic users endpoints
* [ ] Add basic auth scenario
* [ ] Add Swagger/OpenAPI documentation
* [ ] Add Dockerfile
* [ ] Add `.env.example`
* [ ] Deploy API
* [ ] Connect API to `api.azealabs.com`

### Initial Endpoints

```text
GET /health
POST /auth/login
POST /auth/logout
GET /users
POST /users
PUT /users/{id}
DELETE /users/{id}
```

### Completion Criteria

This epic is complete when the API is public, documented, and usable for automation practice.

---

## 10. Epic 8 - Automation Examples

### Goal

Create automation examples that use QA Labs as the target platform.

### Tasks

* [ ] Create `automation-examples` repository
* [ ] Create Selenium folder
* [ ] Create Cypress folder
* [ ] Create Playwright folder
* [ ] Create Robot Framework folder
* [ ] Create Postman folder
* [ ] Add first Selenium login test
* [ ] Add first Cypress login test
* [ ] Add first Playwright login test
* [ ] Add first Robot Framework login test
* [ ] Add README instructions

### Completion Criteria

This epic is complete when at least one QA Labs scenario has examples in multiple frameworks.

---

## 11. Epic 9 - QA Academy Foundation

### Goal

Prepare the future educational side of AZea Labs.

### Tasks

* [ ] Define academy positioning
* [ ] Define first course idea
* [ ] Define target student profile
* [ ] Define course prerequisites
* [ ] Define how QA Labs will be used in lessons
* [ ] Define possible monetization model
* [ ] Define first Selenium course outline

### Completion Criteria

This epic is complete when the first academy direction is documented.

---

## 12. Epic 10 - Future Projects

### Goal

Document future projects that will help improve development and architecture skills.

### Possible Tasks

* [ ] Define Coffee Journal idea
* [ ] Define Music Collection idea
* [ ] Define Travel Journal idea
* [ ] Define HomeLab Dashboard idea
* [ ] Define future mobile/tablet direction
* [ ] Define how future projects connect to AZea Labs

### Completion Criteria

This epic is ongoing and will evolve over time.

---

## 13. Immediate Next Tasks

The next immediate tasks are:

```text
1. Complete this backlog document.
2. Create first ADR documents.
3. Create the `portfolio` repository.
4. Initialize the Astro portfolio project.
5. Create the first version of the homepage.
6. Deploy the first version to Cloudflare Pages.
7. Connect `azealabs.com`.
```

---

## 14. Priority Order

### Priority 1

```text
Finish Sprint 0 documentation.
```

### Priority 2

```text
Create and deploy portfolio MVP.
```

### Priority 3

```text
Plan QA Labs MVP.
```

### Priority 4

```text
Build QA Labs MVP.
```

### Priority 5

```text
Create automation examples.
```

### Priority 6

```text
Prepare QA Academy.
```

---

## 15. Backlog Philosophy

The backlog should remain flexible.

Tasks may change as the project becomes clearer.

The purpose of this backlog is not to predict everything perfectly.

The purpose is to create a professional starting point and keep the project moving in the right direction.

The guiding principle is:

```text
Small steps.
Clear purpose.
Professional execution.
Continuous learning.
```

