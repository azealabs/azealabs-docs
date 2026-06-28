# ADR 0002 - Use Subdomains for Product Separation

## Status

Accepted

## Context

The AZea Labs ecosystem will include multiple products.

Initial and future products include:

* Portfolio
* QA Labs
* QA Academy
* API services
* Documentation
* Future projects

Each product has a different purpose and may eventually use different technologies, deployments, and structures.

The ecosystem needs a clear domain strategy that keeps products separated but connected under one brand.

## Decision

Use `azealabs.com` as the main domain and use subdomains to separate products.

Initial structure:

```text
azealabs.com              -> Portfolio and main hub
labs.azealabs.com         -> QA Labs practice platform
academy.azealabs.com      -> Future QA Academy
api.azealabs.com          -> Backend/API services
docs.azealabs.com         -> Future documentation
```

## Reasoning

Subdomains provide a clean separation between products.

This approach allows each product to:

* Have a clear responsibility.
* Be deployed independently.
* Use different technologies if needed.
* Scale independently.
* Stay connected under the AZea Labs brand.

This avoids mixing the portfolio, practice platform, academy, and APIs into one large application too early.

## Consequences

### Positive

* Clear product separation.
* Professional structure.
* Easier future scaling.
* Lower initial cost because only one domain is needed.
* Better organization for deployment and DNS.

### Negative

* DNS setup may require more configuration.
* Users may need to understand the difference between each subdomain.

## Final Decision

AZea Labs will use `azealabs.com` as the main domain and subdomains for product separation.
