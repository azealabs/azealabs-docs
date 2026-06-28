# AZea Labs - Domain Strategy

## 1. Domain Strategy Overview

This document defines the domain and subdomain strategy for the AZea Labs ecosystem.

The main goal is to use one primary domain as the central brand and then organize future products through subdomains.

Main domain:

```text
azealabs.com
```

This domain will be the main entry point for the ecosystem.

---

## 2. Main Domain

The main domain is:

```text
azealabs.com
```

Purpose:

* Serve as the official AZea Labs website.
* Present Antonio Zea professionally.
* Act as the central portfolio and brand hub.
* Link to all current and future products.
* Provide access to QA Labs, QA Academy, blog, documentation, and future projects.

Initial usage:

```text
azealabs.com -> AZea Labs Portfolio
```

---

## 3. Subdomain Strategy

AZea Labs will use subdomains to separate products clearly.

Recommended structure:

```text
azealabs.com              -> Main portfolio and brand hub
labs.azealabs.com         -> QA Labs practice platform
academy.azealabs.com      -> Future QA Automation academy
api.azealabs.com          -> Backend/API services
docs.azealabs.com         -> Public technical documentation
blog.azealabs.com         -> Optional future blog
```

This structure allows each product to grow independently while staying connected to the AZea Labs brand.

---

## 4. Product Domains

### 4.1 Portfolio

```text
azealabs.com
```

Purpose:

* Main professional website.
* Personal and technical portfolio.
* Central hub for all products.
* First website to be deployed.

---

### 4.2 QA Labs

```text
labs.azealabs.com
```

Purpose:

* Practice platform for QA Automation.
* Demo web pages.
* API testing scenarios.
* Automation challenges.
* Practice target for Selenium, Cypress, Playwright, Robot Framework, and other tools.

QA Labs should remain separate from the portfolio.

---

### 4.3 QA Academy

```text
academy.azealabs.com
```

Purpose:

* Future educational platform.
* Courses and learning material.
* Automation-focused teaching.
* Uses QA Labs as the practice environment.

QA Academy should remain separate from QA Labs.

---

### 4.4 API

```text
api.azealabs.com
```

Purpose:

* Backend APIs for QA Labs and future products.
* REST API endpoints.
* Authentication.
* Test data.
* Future OpenAPI/Swagger documentation.

Initial API examples:

```text
api.azealabs.com/auth
api.azealabs.com/users
api.azealabs.com/products
api.azealabs.com/orders
api.azealabs.com/challenges
```

---

### 4.5 Documentation

```text
docs.azealabs.com
```

Purpose:

* Future public documentation.
* Technical guides.
* QA Labs usage instructions.
* API documentation.
* Automation examples.

At the beginning, documentation will live in GitHub Markdown files.

A public documentation site can be created later.

---

## 5. Why Use Subdomains?

Using subdomains provides several benefits:

* Clear product separation.
* Better organization.
* Professional structure.
* Easier deployment management.
* Each product can use a different technology if needed.
* Each product can scale independently.
* The ecosystem remains connected under one brand.

Example:

```text
azealabs.com
```

is the main brand.

```text
labs.azealabs.com
```

is a product.

```text
academy.azealabs.com
```

is another product.

This avoids mixing everything into one large website.

---

## 6. Initial Deployment Priority

The first domain to deploy is:

```text
azealabs.com
```

This will host the AZea Labs Portfolio.

The second domain to deploy is:

```text
labs.azealabs.com
```

This will host the first version of QA Labs.

The third domain may be:

```text
api.azealabs.com
```

This will be used when QA Labs needs a backend API.

The academy domain should come later:

```text
academy.azealabs.com
```

---

## 7. DNS Strategy

The domain was purchased through Porkbun.

Possible DNS strategy:

```text
Porkbun domain registration
Cloudflare DNS management
Cloudflare Pages deployment
```

Recommended approach:

1. Keep the domain registered in Porkbun.
2. Use Cloudflare for DNS management.
3. Use Cloudflare Pages or Vercel for frontend deployments.
4. Use Render or Railway for backend deployment later.
5. Use Neon or Supabase for PostgreSQL later.

This gives flexibility and keeps costs low.

---

## 8. SSL and HTTPS

All public AZea Labs websites should use HTTPS.

Expected public URLs:

```text
https://azealabs.com
https://labs.azealabs.com
https://academy.azealabs.com
https://api.azealabs.com
https://docs.azealabs.com
```

Cloudflare, Vercel, Render, Railway, and similar platforms can provide HTTPS support.

No separate paid SSL certificate should be purchased at the beginning.

---

## 9. Email Strategy

Email is not required for the first version.

Possible future email addresses:

```text
contact@azealabs.com
hello@azealabs.com
antonio@azealabs.com
support@azealabs.com
academy@azealabs.com
```

Initial recommendation:

* Do not pay for email hosting yet.
* First focus on portfolio deployment.
* Add professional email later when the portfolio or academy needs it.

Possible future providers:

* Google Workspace
* Zoho Mail
* Proton Mail
* Cloudflare Email Routing

---

## 10. Future Domain Possibilities

In the future, if QA Labs grows as an independent product, it may be useful to buy a separate domain.

Possible future domains:

```text
qalabs.dev
qalabs.io
qalabs.app
```

However, this is not necessary at the beginning.

The current strategy is:

```text
Use azealabs.com as the main domain.
Use subdomains for products.
Buy additional domains only if there is a strong reason.
```

---

## 11. Current Domain Decision

The current domain decision is:

```text
Use azealabs.com as the main domain for the AZea Labs ecosystem.

Use subdomains to separate products:

azealabs.com              -> Portfolio
labs.azealabs.com         -> QA Labs
academy.azealabs.com      -> QA Academy
api.azealabs.com          -> API
docs.azealabs.com         -> Documentation
```

This strategy keeps the ecosystem professional, organized, affordable, and ready for future growth.

