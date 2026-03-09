# 20260304 LiNKsites PRD

Status: Draft for review  
Business line: LiNKsites  
Document type: Product Requirements Document  
Planning basis: Updated to approved package model and operating architecture.

## 1. Product Overview

LiNKsites is a template-first website factory that delivers pre-built websites plus managed hosting and operating services through three packages: Standard, Premium, and Enterprise.

## 2. Background and Current State

- Workspace exists at `/Users/linktrend/Projects/Dev_Sites`.
- Existing assets include central Payload CMS, shared frontend templates, factory scripts, deployment guides, and operating SOPs.
- LiNKsites is the most launch-ready cash-flow line in the studio.

## 3. Problem Statement

Target SMBs often face three issues:

- websites that do not convert,
- fragmented vendors and unclear ownership,
- slow and costly custom-agency delivery models.

LiNKsites solves this by combining pre-built site production and managed operations under clear package boundaries.

## 4. Goals

- deliver repeatable website outcomes with controlled support burden,
- standardize package scope and pricing,
- maintain high recurring gross margin while preserving quality,
- establish a sales engine that starts from pre-built proof,
- create a clean upsell path to LiNKautowork and LiNKbots.

## 5. Non-Goals

- unlimited bespoke agency work,
- uncontrolled package customization,
- multi-locale rollout before first-locale density target,
- infrastructure scaling ahead of validated demand.

## 6. Users and Personas

- SMB service businesses in first launch locale (US or Japan),
- businesses requiring managed execution rather than tooling-only products,
- customers likely to grow into automation and advanced service layers.

## 7. Primary Use Cases

- Standard package: lightweight shared-runtime website operations.
- Premium package: richer shared-runtime website with blog and service allowances.
- Enterprise package: dedicated-runtime website with priority support and expanded service allowances.

## 8. Functional Requirements

- package definitions must be explicit and contract-safe,
- site factory workflow must be template-driven and repeatable,
- LiNKbot workflows must support lead generation, CRM updates, and operational orchestration,
- delivery workflow must include QA gate before production handoff,
- overage and capacity-event logic must be enforceable and auditable.

Required workflow stages:

1. lead research and qualification,
2. CRM insertion and prioritization,
3. template adaptation and prebuild,
4. internal QA and package fit check,
5. close and provisioning,
6. managed operations and upsell lifecycle.

## 9. Non-Functional Requirements

- reliability aligned to package commitments,
- secure credential handling and tenant isolation controls,
- observability for rapid incident diagnosis,
- maintainability through templates and SOP-driven operations,
- scalability with locale and package gating logic.

## 10. Architecture and Integrations

- shared control-plane for CMS and operations,
- shared runtime droplets for Standard and Premium tiers,
- dedicated runtime for Enterprise tier,
- Payload CMS for content and tenant control,
- Supabase-backed data layer,
- CRM integration for lead and pipeline lifecycle,
- LiNKbot orchestration for repetitive execution paths,
- LiNKautowork integrations for service allowances.

## 11. Data, Security, and Compliance

- least-privilege access model for all production services,
- separation of customer and internal operational contexts,
- incident and access logging for material operational events,
- review of local legal/data requirements before opening second locale.

## 12. Current and Future Development Needed

Current priorities:

- finalize package UX and contract-ready terms,
- harden LiNKbot-to-CRM lead flow and operational handoffs,
- improve automated provisioning and post-sale checklist enforcement,
- strengthen package usage telemetry for overage and support analytics.

Future priorities:

- broader template coverage by niche,
- tighter conversion and funnel analytics by package,
- stronger automated domain and migration tooling.

## 13. Roadmap Phases

Phase 1:

- launch first locale with package discipline,
- close first paying cohort and validate delivery loop.

Phase 2:

- optimize support, margin, and overage recovery,
- improve conversion via template and process refinements.

Phase 3:

- open second locale after first reaches 20 active sites,
- scale only package lanes with stable quality and economics.

## 14. Acceptance Criteria

- all three packages can be explained, sold, delivered, and supported with documented workflows,
- package economics and support burden are measurable by dashboard,
- LiNKbot-driven lead and CRM workflow is operating reliably,
- overage and capacity-event policies are operationally enforceable.

## 15. Open Questions

- which vertical templates should receive first expansion investment,
- where to set strict customization boundaries by package,
- what SLA and response-time guarantees should be formalized per package tier.
