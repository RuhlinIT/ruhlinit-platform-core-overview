# RuhlinIT Platform Core

**RuhlinIT Platform Core**, or **RPC**, is the reusable technology foundation behind RuhlinIT’s growing digital products, services, and software platforms.

It is designed as a private internal platform for building, testing, documenting, and launching reusable software capabilities across multiple RuhlinIT brands and future products.

This public repository is a high-level overview only.

The full implementation remains private.

---

## What This Project Is

RuhlinIT Platform Core is a reusable platform foundation focused on:

- shared architecture patterns
- reusable frontend modules
- reusable backend services
- provider-agnostic contracts
- database and migration standards
- testing and quality gates
- documentation standards
- infrastructure patterns
- optional integration adapters
- product and audience isolation
- local-first MVP development
- reusable document and export patterns
- workflow and automation foundations

The goal is to build software once in a clean, reusable way, then adapt it safely across multiple products without copy-pasting fragile one-off code.

---

## What This Project Is Not

RuhlinIT Platform Core is **not**:

- one giant all-in-one application
- a public SaaS product by itself
- a blended database for unrelated products
- a vendor-locked platform
- a collection of unfinished experiments
- a place for product-specific business logic to leak into shared code
- a single shared runtime for every RuhlinIT idea
- a replacement for focused product-specific applications

The platform is intentionally designed around clean boundaries.

Reusable core capability belongs in the platform.

Product-specific behavior belongs in product adapters.

Project-specific implementation belongs in the final app.

---

## Architecture Philosophy

RuhlinIT Platform Core follows a strict build order:

1. Core platform-native capability
2. Provider-agnostic contract
3. Open-standard fallback
4. Manual or self-hosted fallback
5. Optional external provider adapter
6. Product-specific adapter
7. Project-specific business logic

This keeps the platform flexible, portable, and resistant to vendor lock-in.

External services such as CRM tools, productivity platforms, payment providers, cloud providers, automation tools, communication platforms, and AI services should enhance the platform only where useful. They should not become required for the core capability to work.

---

## Current Technology Direction

The current internal implementation is built around a modern full-stack architecture.

Frontend direction:

```txt
React
TypeScript
Vite
Nx
Reusable feature packages
CSS Modules where useful
```

Backend direction:

```
Java
Spring Boot
Gradle
Provider-agnostic service boundaries
```

Database direction:

```
PostgreSQL
Flyway migrations
Native persistence first
```

Testing direction:

```
Unit tests
Component tests
API tests
End-to-end tests
Accessibility-aware UI testing
Quality gates before module completion
```

Infrastructure direction:

```
Docker
Docker Compose
GitHub
GitHub Actions planned
Cloud-provider flexibility
Terraform where useful
```

## Working Reference Modules

RPC is being built through real working slices instead of abstract architecture alone.

The current internal reference modules are:

```txt
Web Presence + Lead Capture
Re-zume Local Resume/CV/Application Pipeline
```

Each module proves reusable platform patterns that can later be adapted across other products or brands.

## Reference Module 1: Web Presence + Lead Capture

The first internal reference module is a reusable Web Presence + Lead Capture slice.

It proves the platform pattern across:

```
shared contracts
→ reusable React feature package
→ web app integration
→ native Spring Boot API
→ PostgreSQL persistence
→ migration-controlled schema
→ automated tests
```

This module demonstrates how a reusable platform capability can be built once and then adapted across different products or sites.

The public overview does not include private implementation details, internal repo paths, credentials, operational setup, or business-specific lead workflows.

---

## Reference Module 2: Re-zume Local Resume/CV/Application Pipeline

The second internal reference module is Re-zume, a local resume, cover letter, and job application pipeline.

Re-zume exists to help generate tailored job application materials quickly while proving reusable RPC patterns for document generation, structured profile data, application tracking, local-first workflows, and export-ready UI.

It demonstrates platform reuse across:

```txt
structured career profile contracts
→ target job and application contracts
→ resume variant generation
→ cover letter generation
→ job description parsing
→ local application tracking
→ styled document previews
→ plain text copy
→ rich formatted copy
→ browser-based PDF export
→ component and feature tests
```

Re-zume is currently treated as a local-first productivity MVP, not a public SaaS product.

Its internal implementation explores reusable platform patterns for:

- career profile data
- target job records
- application status tracking
- resume variant generation
- cover letter generation
- rule-based job description parsing
- document preview styling
- export-safe global document classes
- print/PDF workflows
- reusable formatter logic
- component-level testing

The public overview does not include private resume seed data, internal job history details, private implementation paths, generated application records, or personal job application workflows.

# Core Design Principles
## Native capability first

Every module should work through the platform’s own native implementation before external integrations are added.

## Provider-agnostic contracts

Core contracts should not depend on any one vendor, CRM, cloud provider, payment processor, AI provider, or productivity tool.

## Local-first where practical

Early MVPs should work locally before requiring hosted infrastructure, paid services, or external integrations.

## Exportable, portable data

Where practical, generated documents, records, and workflows should support export, backup, and migration paths.

## Optional adapters

External integrations should be optional adapters, not hard dependencies.

## Product isolation

Each product, brand, or audience-specific platform should remain cleanly separated.

## Reusable modules

Shared capabilities should be packaged, documented, tested, and reused instead of copied between apps.

## Documentation as a first-class asset

Each meaningful module should have product notes, technical notes, API contracts, schema guides, rollout guidance, quality checklists, and extraction notes.

## Tests before scale

The platform should not expand faster than its quality gates.

## Example Module Categories

RuhlinIT Platform Core is intended to support reusable modules across areas such as:

- web presence
- lead capture
- publication and visibility controls
- profile and identity-adjacent features
- media and upload workflows
- reusable form patterns
- API contract patterns
- database schema patterns
- integration adapters
- documentation generators
- workflow foundations
- product-specific adapters
- future platform factory capabilities
- resume and document generation
- cover letter and application packet workflows
- job parsing and structured extraction
- local-first application tracking

Not every module exists yet. The platform is being built incrementally, starting with small working slices.

## Public vs Private Scope

This public repository or README may describe:

- high-level architecture
- public-safe roadmap themes
- technology direction
- design principles
- module categories
- progress summaries
- portfolio-safe implementation notes
- non-sensitive reference module summaries

The private repository contains:

- source code
- detailed implementation
- local development setup
- internal infrastructure details
- private database configuration
- private roadmap notes
- business-specific adapters
- internal documentation
- test suites
- operational scripts
- personal seed data
- private application records

## Why This Exists

RuhlinIT works across multiple digital services, brands, and software ideas.

A reusable platform core helps avoid rebuilding the same foundations repeatedly.

Instead of each product having its own disconnected implementation for forms, data models, APIs, workflows, integrations, document generation, and documentation, RuhlinIT Platform Core creates a shared foundation that can be adapted cleanly.

This supports faster product development while keeping quality, maintainability, and architectural discipline in place.

## Development Status

RuhlinIT Platform Core is currently in early internal development.

Current focus:

```txt
RPC v0.1
Reusable platform foundations
Working vertical slices
Documentation standards
Testing standards
Native-first architecture
Local-first MVP patterns
```

Completed internally:

```txt
Reusable lead capture contract pattern
Reusable React feature package pattern
Native Spring Boot API pattern
PostgreSQL persistence pattern
Flyway migration pattern
Frontend and backend testing pattern
End-to-end browser flow pattern
Local resume/CV pipeline pattern
Resume variant generation pattern
Cover letter generation pattern
Rule-based job parser pattern
Application tracker pattern
Document preview and PDF export pattern
Component test pattern for generated documents
```

Deferred intentionally:

```txt
Public SaaS launch
Marketplace system
Advanced analytics
AI scoring
AI-assisted rewriting
CRM automation
Payment workflows
Large admin dashboards
Public plugin ecosystem
Hosted multi-user application tracking
Automated job board submission
Browser extension workflows
```

Those areas may be explored later only after the core platform remains stable, tested, and well documented.

## Relationship to Future Products

RuhlinIT Platform Core is designed to support multiple future products and brands without blending their audiences, data, or business rules together.

Future product lines may consume platform patterns while keeping their own:

- app or site
- database where appropriate
- domain
- user experience
- audience
- content model
- integrations
- governance model
- brand-specific behavior

This allows reuse without contamination.

## Example Future Product Areas

RPC may eventually support internal or public-facing systems across areas such as:

- business websites
- lead capture and CRM intake
- digital profile systems
- resume and career tooling
- documentation generators
- event operations
- haunt operations
- creative asset workflows
- workflow automation
- business rules and data dictionary tools
- product launch systems
- application tracking
- training and tutorial generators
- provider-agnostic integration hubs

These areas are expected to remain separate products or modules, not one blended application.

## Guiding Standard

The guiding standard for this project is simple:

```
Build reusable capability once, keep it clean, test it well, document it clearly, and adapt it safely.
```

## About RuhlinIT

RuhlinIT is a technology and creative solutions company focused on turning ideas into working systems, digital products, automation workflows, branded experiences, and reusable software foundations.

RuhlinIT Platform Core is part of that long-term internal platform strategy.

## Contact

For questions about RuhlinIT, digital product development, platform architecture, or future collaboration, contact RuhlinIT through the appropriate public business channels.