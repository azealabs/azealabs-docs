# AZea Labs - GitHub Strategy

## 1. GitHub Strategy Overview

This document defines how GitHub will be used for the AZea Labs ecosystem.

GitHub will be the central place for:

* Source code
* Documentation
* Architecture decisions
* Roadmap
* Issues
* Pull requests
* Releases
* CI/CD workflows
* Automation examples

The goal is to use GitHub not only as a code repository, but as a professional project management and engineering platform.

---

## 2. GitHub Organization

The GitHub organization is:

```text
azealabs
```

Purpose:

* Keep AZea Labs projects separated from personal repositories.
* Present the ecosystem professionally.
* Organize repositories by product.
* Make the project easier to scale in the future.
* Show a professional engineering workflow.

---

## 3. Initial Repository

The first repository is:

```text
azealabs-docs
```

Purpose:

* Store the main project documentation.
* Define the ecosystem vision.
* Define architecture.
* Define roadmap.
* Document technical decisions.
* Plan future products.

This repository is the foundation of the AZea Labs ecosystem.

---

## 4. Future Repositories

Recommended future repositories:

```text
portfolio
qalabs-web
qalabs-api
automation-examples
qa-academy
shared-ui
```

### 4.1 portfolio

Purpose:

* Source code for `azealabs.com`.
* Main professional portfolio.
* Brand hub for all AZea Labs products.

Suggested stack:

```text
Astro
TypeScript
Tailwind CSS
Cloudflare Pages
```

---

### 4.2 qalabs-web

Purpose:

* Frontend application for QA Labs.
* Demo pages for automation practice.
* UI for web testing scenarios.

Suggested stack:

```text
Next.js
TypeScript
Tailwind CSS
```

---

### 4.3 qalabs-api

Purpose:

* Backend API for QA Labs.
* Authentication scenarios.
* API testing scenarios.
* Test data.
* Future challenge/reporting features.

Suggested stack:

```text
Python
FastAPI
PostgreSQL
Docker
```

---

### 4.4 automation-examples

Purpose:

* Automation examples that target QA Labs.
* Examples by framework.

Possible structure:

```text
automation-examples/
├── selenium/
├── cypress/
├── playwright/
├── robot-framework/
└── postman/
```

---

### 4.5 qa-academy

Purpose:

* Future educational platform.
* Course pages.
* Learning paths.
* Material connected to QA Labs exercises.

---

### 4.6 shared-ui

Purpose:

* Future shared design system.
* Reusable components.
* Shared styles.
* Common branding elements.

This repository is optional and should only be created when multiple products need shared UI components.

---

## 5. Repository Creation Order

Recommended order:

```text
1. azealabs-docs
2. portfolio
3. qalabs-web
4. qalabs-api
5. automation-examples
6. qa-academy
7. shared-ui
```

The next repository to create is:

```text
portfolio
```

Reason:

* The portfolio is the first public product.
* It will deploy to `azealabs.com`.
* It will act as the central hub for future products.

---

## 6. Branching Strategy

At the beginning, the branching strategy should be simple.

Recommended branches:

```text
main
develop
feature/*
```

### main

Purpose:

* Production-ready code.
* Deployed version.
* Stable releases.

### develop

Purpose:

* Integration branch.
* Work that is almost ready but not yet released.

### feature branches

Format:

```text
feature/short-description
```

Examples:

```text
feature/home-page
feature/about-section
feature/projects-section
feature/contact-section
```

For very small projects, it is acceptable to work directly with `main` at the beginning, but the professional target should be to use feature branches and pull requests.

---

## 7. Pull Request Strategy

Pull requests should be used to review changes before merging into `main`.

Each pull request should include:

* Summary of changes.
* Screenshots if UI changed.
* Testing notes.
* Related issue if applicable.

Pull request template may be added later.

Initial PR checklist:

```text
- [ ] Code builds successfully
- [ ] UI was reviewed visually
- [ ] No secrets were committed
- [ ] Documentation was updated if needed
- [ ] Tests were added or updated if applicable
```

---

## 8. Commit Message Strategy

Commit messages should be clear and descriptive.

Recommended format:

```text
type: short description
```

Examples:

```text
docs: add master plan
docs: add roadmap
feat: add homepage hero section
feat: add projects section
fix: correct responsive layout
refactor: improve component structure
chore: update dependencies
```

Common types:

```text
docs
feat
fix
refactor
chore
test
style
ci
```

The goal is to keep Git history readable and professional.

---

## 9. Issues Strategy

GitHub Issues will be used to organize work.

Issue types:

```text
Feature
Bug
Documentation
Architecture
Research
Task
Improvement
```

Example issues:

```text
Create portfolio homepage
Create About section
Research Astro deployment on Cloudflare Pages
Design QA Labs MVP scenarios
Create login demo specification
Define API endpoint structure
```

Issues should be small enough to complete in a reasonable amount of time.

---

## 10. Labels Strategy

Suggested labels:

```text
type: feature
type: bug
type: docs
type: research
type: architecture
type: improvement

status: backlog
status: in-progress
status: blocked
status: review
status: done

priority: low
priority: medium
priority: high

product: portfolio
product: qalabs
product: academy
product: docs
```

Labels help organize the work as the ecosystem grows.

---

## 11. Milestones Strategy

Milestones should represent meaningful project stages.

Initial milestones:

```text
Sprint 0 - Foundation
Portfolio v0.1
Portfolio v0.2
QA Labs MVP
QA Labs API v0.1
Automation Examples v0.1
QA Academy Foundation
```

Each milestone should group related issues.

---

## 12. GitHub Projects Strategy

A GitHub Project board may be created later.

Recommended columns:

```text
Backlog
Ready
In Progress
Review
Done
```

This will help manage work visually.

At the beginning, the documentation repository and issues are enough.

A project board becomes more useful once development starts.

---

## 13. Releases Strategy

Releases should be used when a product reaches an important version.

Example releases:

```text
portfolio-v0.1
portfolio-v0.2
qalabs-v0.1
qalabs-api-v0.1
```

Each release should include:

* Summary
* New features
* Fixes
* Known limitations
* Next steps

---

## 14. CI/CD Strategy

GitHub Actions will be used later for CI/CD.

Initial goals:

* Build validation.
* Linting.
* Tests.
* Deployment automation.
* Automation test execution.

Possible workflows:

```text
portfolio-ci.yml
qalabs-web-ci.yml
qalabs-api-ci.yml
automation-tests.yml
```

CI/CD should be added gradually.

The first portfolio version may use Cloudflare Pages automatic deployment from GitHub.

---

## 15. Security Strategy

Basic security rules:

* Never commit secrets.
* Use environment variables.
* Use `.env.example` files.
* Keep dependencies updated.
* Use private values only in platform settings.
* Review pull requests before merging important changes.

Examples of secrets that should never be committed:

```text
DATABASE_URL
JWT_SECRET
API_KEYS
EMAIL_PASSWORD
CLOUDFLARE_TOKEN
GITHUB_TOKEN
```

---

## 16. Documentation Strategy

Documentation should be treated as part of the project, not as an afterthought.

Documentation should include:

* Vision
* Products
* Roadmap
* Architecture
* Tech stack
* Domain strategy
* GitHub strategy
* Backlog
* ADRs
* Setup guides
* Deployment guides
* Testing guides

The `azealabs-docs` repository will remain the central documentation source during the early stages.

---

## 17. ADR Strategy

Architecture Decision Records should be used to document important decisions.

ADR stands for:

```text
Architecture Decision Record
```

Example ADRs:

```text
0001-use-azealabs-as-main-brand.md
0002-use-subdomains-for-products.md
0003-use-astro-for-portfolio.md
0004-use-modular-monolith-for-backend.md
```

Each ADR should explain:

* Context
* Decision
* Consequences

This will help understand why decisions were made.

---

## 18. Current GitHub Decision

The current GitHub decision is:

```text
Use the azealabs GitHub organization as the central engineering workspace.

Start with azealabs-docs for documentation.

Create portfolio as the first code repository.

Use clear commits, issues, documentation, and eventually pull requests and CI/CD.

Grow the GitHub workflow gradually as the ecosystem grows.
```

This supports the AZea Labs philosophy:

```text
Build professionally.
Document decisions.
Learn real engineering workflows.
Prepare to teach later.
```

