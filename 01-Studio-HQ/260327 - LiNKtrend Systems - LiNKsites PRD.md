# Product Requirements Document (PRD)
# LiNKsites — Website Implementation Platform and Factory Kit

Document date: 2026-03-27  
Status: Draft (Phase 2)  
Owner: LiNKtrend Venture Studio  

## 1. Product Summary

LiNKsites is the Venture Studio’s website realization platform: an internal developer platform optimized for fast, governed production of web-presence assets. It exists to transform website creation from bespoke projects into a standardized manufacturing process. In the Venture Studio architecture, LiNKsites is an implementation platform IDP, not a control plane, not a logic authority, and not a memory system. It is the place where validated venture definitions become deployable websites, and it is the infrastructure layer that makes “build-first, sell-later” website commercialization possible at scale.

LiNKsites must support two realities simultaneously. Internally, it must allow LiNKtrend to deploy venture websites and campaign surfaces rapidly with consistent standards for SEO, localization, performance, and compliance. Externally, it must support a productized website factory business line where pre-built demos can be created and shown to prospects, sold, and then operated under clear package boundaries. The platform must remain the platform; monetization models are layered on top of it.

## 2. Context and Problem Statement

Most SMB website delivery models fail economically because they are custom by default. Agencies repeatedly rebuild the same structures, repeatedly manage the same legal and compliance surfaces, and repeatedly perform the same deployment and maintenance tasks. The result is high labor cost, inconsistent quality, slow delivery, and fragile operations. From the Venture Studio perspective, these failures are unacceptable because websites are a recurring need across ventures and across commercialization lines. If the factory must reinvent websites every time, marginal cost never approaches zero.

LiNKsites exists to eliminate repeated reinvention. It standardizes templates and content models, centralizes content operations through a single CMS, enforces multi-site scoping and governance rules, and supports deployment topologies that balance cost efficiency with isolation when required. It must also support a world in which websites are not only human-facing but machine-facing: search, AI-assisted discovery, and citation readiness require structured data, consistent content modeling, and policy-compliant legal surfaces.

## 3. Objectives and Success Criteria

LiNKsites must allow agents to create a functional, compliant, fast website instance quickly without making fundamental architectural decisions each time. It must allow a single centralized CMS to govern a fleet of sites, including domain mappings, shared legal pages, and structured content entities. It must support a shared runtime mode that can serve many sites cheaply and a dedicated runtime mode for clients who require isolation. It must support multi-language operation and enforce site-scoped data boundaries so that content from one site cannot bleed into another.

LiNKsites is successful when a new site can be created as a deterministic manufacturing act, when content can be updated centrally with predictable propagation, when compliance surfaces can be maintained without per-site manual work, and when the operational burden of maintaining many sites does not scale linearly with site count. Commercially, it is successful when demos can be produced quickly, sold, and operated under package discipline without collapsing into bespoke support chaos.

## 4. Users and Actors

Internally, the primary “users” are the Venture Studio itself: LiNKaios triggers site production; LiNKbots execute production and operations; LiNKautowork runs provisioning and ritual workflows; LiNKskills provides governed logic for repeatable tasks; LiNKbrain stores audit records and learned patterns. Human operators exist as governance and exception handlers, not as primary builders.

Externally, the primary users are SMB clients who purchase a website under clear package boundaries. They interact with the outcome (the website) and may have limited CMS access depending on package policy. External commercialization also introduces sales and operations roles in the workforce (client acquisition, onboarding, support, and incident response).

## 5. Scope and Boundaries

LiNKsites is responsible for: template-first website production; centralized CMS governance; multi-site scoping and data isolation; structured content models; shared legal and common pages; localization support; SEO and performance baselines; deployment conventions; and the integration surfaces that allow automations and bots to create, configure, and operate sites deterministically.

LiNKsites is not responsible for: orchestration of missions and tasks (LiNKaios), reusable procedural logic governance (LiNKskills), persistent memory and audit truth beyond its own domain artifacts (LiNKbrain), deterministic workflow execution (LiNKautowork), or application product realization (LiNKapps). LiNKsites must also not become an unbounded custom development environment; customization must be constrained by template evolution rules so that the platform compounds rather than fragments.

## 6. Core Concepts and Objects

### 6.1 Site and Site Identifier

A site is a tenant-scoped website instance. Every content entity and configuration entity must be associated with a site identifier. Site identifiers are the primary boundary for data isolation in the multi-site fleet.

### 6.2 Domain Mapping

In shared runtime mode, the runtime resolves a request’s hostname to a site identifier through CMS-managed domain mappings. This makes domain name a deterministic selector for site context and allows one runtime to serve many sites without cloning codebases per customer.

### 6.3 Templates and Template Variants

Templates are governed starting architectures that encode page structures, blocks, layouts, component usage patterns, content schema expectations, and operational defaults. Templates must support evolution through controlled promotion so improvements become platform assets rather than isolated client hacks.

### 6.4 Central CMS as Control Surface

The CMS is not merely a page editor. It is the command layer for fleet governance: content modeling, site-scoped administration, domain mapping, shared pages, publishing controls, and operational triggers.

## 7. Functional Requirements

### 7.1 Template-First Site Creation

The platform must support deterministic creation of a new site from a selected template, including seeding a minimum working set of pages and entities required for a functional demo. Site creation must also create domain mappings and default configuration state so the site can be served immediately.

### 7.2 Centralized Content Governance

All content must be managed through centralized schemas so that the platform can enforce consistency across the fleet. The system must support shared content constructs (notably legal pages) that can be maintained centrally and propagated.

### 7.3 Multi-Site Isolation and Safe Public Reads

Public traffic must only be able to read published content under a resolved site context. The system must enforce that public reads are site-scoped and cannot enumerate or access content for other sites. Admin reads and writes must be role-bound and auditable.

### 7.4 Localization and Multi-Language Operation

The platform must support multiple locales per site with stable routing patterns. The system must enforce that localized content is retrieved under both site and locale scopes so the correct variant is served.

### 7.5 Hosting Modes (Shared and Dedicated)

The platform must support a shared runtime mode where one deployment serves many sites by hostname and a dedicated runtime mode where a client receives an isolated deployment locked to a single site identifier while still using the central CMS and database by site context. This enables both low-cost volume operations and higher-margin isolation offerings.

### 7.6 Operational Update and Automation Integration

The platform must support automation-driven updates, including content updates, provisioning flows, and scheduled publishing patterns. Automations must interact with the CMS and database through governed interfaces and must produce auditable events and records.

## 8. Non-Functional Requirements

LiNKsites must enforce performance and SEO baselines. It must avoid template drift that produces inconsistent UX. It must support observability and incident diagnosis for both the shared runtime and dedicated deployments. It must support secure secrets handling and least privilege. It must be maintainable as the fleet scales, meaning that central changes must be able to propagate safely without breaking unknown client sites.

## 9. Roadmap by Phase

### 9.1 MVP (MVO)

The MVP delivers an internal website factory kit capable of producing and serving demo sites under a shared runtime with a central CMS and Supabase-backed database. It delivers template-first site creation, domain mapping, a minimum content schema set, localization scaffolding, and operational runbooks for deployment. It supports creation of demos, attaching domains for paying clients, and basic monitoring and incident response.

### 9.2 PMF

The PMF phase productizes the platform into an external website factory line with package discipline. It strengthens automation-driven provisioning, improves content and legal propagation, adds stronger observability and release discipline for shared runtime deployments, expands template coverage, and improves the sales-to-delivery loop (lead intake, demo generation, close, provisioning, and operations).

### 9.3 Full-Scale

Full-scale LiNKsites supports multi-locale expansion, mature governance for shared assets (legal-as-code and fleet-wide policy updates), high-throughput template evolution and certification, and robust multi-tenant commercialization. It supports a fleet large enough that operations and updates must be managed with strong change-control and rollback mechanisms, and it integrates deeply with LiNKautowork and LiNKskills to reduce manual operational burden further.

## 10. Appendix: Phase 1 Truth Sources

This PRD is written as a from-zero product definition, but it must align with Phase 1 truth sources, including:

- Venture Studio process authority: `/Users/linktrend/Projects/LiNKsmartfile/01-Studio-HQ/260326 - LiNKtrend Venture Studio Building Process.md`
- LiNKsites reference implementation: `/Users/linktrend/Projects/LiNKsites`
- LiNKsites supporting documentation in this repo: `/Users/linktrend/Projects/LiNKsmartfile/00-Reference-Material/1-LiNKsites`
