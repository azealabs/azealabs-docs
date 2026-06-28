# ADR 0004 - Use Next.js for QA Labs Frontend

## Status

Accepted

## Date

2026-06-28

## Context

QA Labs will be the first major product under the AZea Labs ecosystem.

Unlike the main AZea Labs portfolio, QA Labs will not be only a static website. It will need interactive pages, demo workflows, stateful UI behavior, API integration, dynamic examples, and future support for authentication-like scenarios.

The frontend needs to support:

```text
Demo pages for automation practice
Interactive UI components
Forms, tables, filters, uploads, downloads, and dashboards
Stable selectors for automation
Scenario documentation
Future API integration
Future authentication flows
Future expansion into a larger product
```

The frontend should also be approachable, maintainable, and aligned with modern frontend development practices.

## Decision

QA Labs frontend will use:

```text
Next.js
TypeScript
Tailwind CSS
```

The initial repository will be:

```text
qalabs-web
```

The planned public URL will be:

```text
https://labs.azealabs.com
```

## Considered Options

### Option 1 - Astro

Astro is already being used for the AZea Labs portfolio and works very well for static content, landing pages, documentation pages, and marketing sites.

However, QA Labs will require more interactive application behavior than the portfolio.

Astro remains the right choice for the portfolio, but it is not the best first choice for the QA Labs web application.

### Option 2 - Vite + React

Vite with React would be lightweight, fast, and flexible.

It would work well for an interactive frontend, but it would require more manual decisions around routing, application structure, metadata, and future deployment conventions.

### Option 3 - Next.js

Next.js provides a strong foundation for React applications, routing, layouts, metadata, server/client boundaries, future API integration patterns, and scalable application structure.

It is widely used in professional frontend development and is suitable for building a product that can grow beyond a simple demo site.

## Rationale

Next.js is selected because QA Labs is expected to grow into a real product, not just a static demo.

The project will benefit from:

```text
File-based routing
React ecosystem support
TypeScript support
Strong layout patterns
Good developer experience
Support for static and dynamic pages
Future authentication support
Future API integration support
Good deployment options
```

Next.js also provides a valuable learning opportunity for building larger frontend applications with modern patterns.

## Consequences

### Positive Consequences

```text
QA Labs will have a scalable frontend foundation
The project can support interactive UI scenarios
The frontend can grow beyond the MVP
The stack is aligned with modern frontend development
The project becomes useful for learning real application architecture
```

### Negative Consequences

```text
Next.js is more complex than a simple static site
There will be more framework concepts to learn
Deployment configuration may require more attention
Some pages may be more complex than necessary in the early MVP
```

## Implementation Notes

The initial frontend should remain simple.

The first version should focus on:

```text
QA Labs landing page
Login Demo page
Forms Demo page
Tables Demo page
Scenario documentation
Stable data-testid selectors
Responsive layout
Deployment to labs.azealabs.com
```

Avoid adding unnecessary complexity during the MVP.

Do not add advanced authentication, payments, dashboards, admin tools, or complex state management in the first version.

## Related Documents

```text
docs/04-architecture.md
docs/05-tech-stack.md
docs/08-backlog.md
docs/09-qalabs-mvp-scope.md
```

## Decision Summary

QA Labs frontend will use **Next.js with TypeScript and Tailwind CSS** because it provides a professional, scalable, and modern foundation for an interactive QA automation practice platform.

