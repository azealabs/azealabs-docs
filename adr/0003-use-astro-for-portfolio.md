# ADR 0003 - Use Astro for the Portfolio MVP

## Status

Accepted

## Context

The first product to build is the AZea Labs Portfolio.

The portfolio needs to be:

* Fast
* Professional
* Easy to maintain
* Good for static content
* Good for future blog content
* Low-cost to deploy
* Simple enough for the first public version

The portfolio does not need a backend in the first version.

## Decision

Use the following stack for the Portfolio MVP:

```text
Astro
TypeScript
Tailwind CSS
Cloudflare Pages
GitHub
```

## Reasoning

Astro is a good fit for the portfolio because the first version will be mostly static content.

It works well for:

* Landing pages
* Portfolio websites
* Blogs
* Documentation-style content
* Fast static websites

TypeScript will help improve code quality.

Tailwind CSS will help create a modern responsive design.

Cloudflare Pages will provide low-cost hosting and GitHub-based deployment.

## Alternatives Considered

### Next.js

Next.js is powerful and may be used later for QA Labs.

However, for the portfolio MVP, it may be more than what is needed.

### Plain HTML/CSS

Plain HTML/CSS would be simple, but it would not provide the same structure, component reuse, and growth path as Astro.

### WordPress

WordPress is not aligned with the goal of learning modern development and architecture through code.

## Consequences

### Positive

* Fast performance.
* Good developer experience.
* Good for future blog content.
* Low-cost deployment.
* Supports reusable components.
* Easier than building a full web application.

### Negative

* Requires learning Astro.
* Some dynamic features may require extra integration later.

## Final Decision

The AZea Labs Portfolio MVP will use Astro, TypeScript, Tailwind CSS, GitHub, and Cloudflare Pages.
