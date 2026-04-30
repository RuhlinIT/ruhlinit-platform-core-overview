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
Media Asset Storage
Collectors Crypt Design Program Watchlist
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

## Reference Module 3: Media Asset Storage

The third internal reference module is a reusable Media Asset Storage slice.

It proves platform patterns for handling uploaded or externally referenced media in a provider-agnostic way.

This module demonstrates reuse across:

```txt
provider-neutral media contracts
→ reusable media ingestion feature
→ local development storage
→ adapter-ready provider architecture
→ private/internal media handling
→ image source attribution
→ safe storage path generation
→ future cloud storage support
```

The current internal implementation supports local media persistence for development and testing. It is structured so future storage providers can be added through adapter modules without changing product-specific workflows.

The public overview does not include private media files, storage credentials, provider tokens, private asset paths, or imported third-party media.

## Reference Module 4: Collectors Crypt Design Program Watchlist

The fourth internal reference module is a private Collectors Crypt research workflow for tracking public design-program-style submissions, creator names, submission metadata, lore, descriptions, specifications, tags, and referenced images.

It demonstrates how a product-specific feature can consume reusable platform services while keeping proprietary product logic isolated.

This module proves the pattern across:

```
product-specific domain contracts
→ product-specific API workflow
→ reusable RPC media ingestion
→ local media persistence
→ React import workflow
→ React gallery/list workflow
→ product shell composition
```

This reference module is intentionally product-specific. Its Collectors Crypt business rules, private scouting workflows, review criteria, and collaboration strategy belong under the product boundary rather than in the reusable platform core.

The public overview does not include private scouting data, downloaded media, private creator notes, internal review records, outreach workflows, or proprietary Collectors Crypt implementation details.

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

## Adapter isolation

External provider behavior should be isolated behind adapters.

Product code should not call external vendor SDKs directly when a reusable platform contract or feature can provide a cleaner boundary.

For example, media storage can support local development first, then later use a provider adapter without rewriting the product workflow.

## Product isolation

Each product, brand, or audience-specific platform should remain cleanly separated.

## Product-specific logic stays out of RPC

RPC should contain reusable contracts, features, and adapters.

Product-specific workflows, business rules, review criteria, scouting logic, UI flows, and proprietary behavior should live under the relevant product boundary.

For example:

```txt
Reusable media ingestion belongs in RPC.
Collectors Crypt submission review logic belongs in Collectors Crypt.
Reusable design components belong in RDC.
```

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
- media asset storage
- image ingestion and persistence
- provider-neutral storage contracts
- local development storage adapters
- cloud storage adapters
- private research workflows
- creator/submission tracking workflows
- filterable gallery and review interfaces

Not every module exists yet. The platform is being built incrementally, starting with small working slices.

## Internal Project Boundary Pattern

The internal implementation follows clear library boundaries.

Reusable platform logic belongs in RPC:

```txt
libs/rpc/contracts
libs/rpc/features
libs/rpc/adapters
```

Product-specific logic belongs under the product namespace:

``` txt
libs/{product-name}/...
```

Design-system logic belongs in RDC or related design libraries:

``` txt
libs/platform-core-ui
libs/platform-core-theme
```

This helps prevent reusable platform code, product-specific business rules, and design-system concerns from blending together.

## RPC Module Pattern

RPC modules are organized into three main types.

```txt
contracts
features
adapters
```
### Contracts

Contracts define provider-neutral TypeScript shapes such as DTOs, request objects, response objects, shared status types, and adapter interfaces.

### Features

Features define reusable platform behavior and orchestration. They may include services, modules, local development implementations, and provider injection points.

### Adapters

Adapters isolate external provider behavior, such as storage providers, CRM tools, cloud services, payment providers, productivity tools, or communication platforms.

This keeps the core platform portable while allowing optional integrations to be added only where useful.

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

In the “This public repository or README may describe” list, add:

```md
- public-safe reference module summaries
- high-level module boundary patterns
- provider-agnostic architecture concepts
- local-first MVP validation patterns
```

In the “The private repository contains” list, add:

```md
- imported or generated media files
- provider tokens or credentials
- product-specific business rules
- private research and review data
- private creator or submission notes
- internal adapter implementation details
```

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
Provider-neutral media asset contract pattern
Reusable media ingestion feature pattern
Local media storage pattern
Adapter scaffold pattern for external storage providers
Product-specific Collectors Crypt domain/API feature pattern
React import panel pattern
React gallery/list scaffold pattern
End-to-end local media ingestion smoke test
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
Production cloud media storage
Public media republishing workflows
Creator outreach automation
Submission scoring automation
Advanced gallery analytics
Automated public website scraping
Hosted multi-user research dashboard
```

Those areas may be explored later only after the core platform remains stable, tested, and well documented.

## Recent Internal Progress

Recent internal work has expanded RPC beyond lead capture and document generation into media handling and product-specific research workflows.

New validated patterns include:

```txt
RPC contract / feature / adapter separation
local media asset ingestion
provider-neutral storage contracts
product-specific API orchestration
product-specific React feature composition
runtime smoke testing across API and web apps
```

This progress reinforces the platform direction: reusable capability is built in RPC, product-specific behavior remains isolated, and external providers are added through optional adapters.

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

Recent internal reference work also validates that product-specific research workflows can consume reusable platform services without forcing those workflows back into the platform core.

For example, a product can use shared media ingestion while keeping its own domain model, review process, UI, data rules, and collaboration strategy isolated.

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
- media repositories
- digital asset storage
- creator and submission research workflows
- private review galleries
- product scouting tools
- provider-agnostic file and image workflows

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