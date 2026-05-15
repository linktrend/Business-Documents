# 20260304 LiNKskills PRD

Status: Draft for review  
Business line: LiNKskills  
Document type: Product Requirements Document  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Product Overview

LiNKskills is a governed intelligence layer that begins as the internal source of truth for all bots and evolves into a multi-tenant API and MCP product.

## 2. Background and Current State

- Current repo exists at `https://github.com/linktrend/LiNKskills-Library`.
- The library already contains catalogued skills, tools, SOPs, validation rules, and product-direction documentation.
- The major next step is converting the governed library into the LiNKskills Logic Engine while still using it internally immediately.

Current development needs:

- The library and standards are real now.
- The missing layer is centralized delivery, tenancy, billing, and product UI or onboarding.
- Internal adoption should start immediately rather than waiting for perfect productization.

## 3. Problem Statement

Copying skills into separate agents creates version drift, weak governance, weak monetization, and poor IP control. LiNKskills solves that by centralizing standards, execution logic, and future commercial access.

## 4. Goals

- Create a product or service line that is commercially clear and operationally repeatable.
- Use shared LiNKtrend infrastructure to reduce time, cost, and quality drift.
- Make the line measurable through operational, quality, and financial KPIs.
- Preserve future expansion paths without overbuilding V1.

## 5. Non-Goals

- Turning the line into unlimited bespoke consulting.
- Supporting every possible market, feature, or edge case in V1.
- Scaling infrastructure ahead of proven demand.
- Breaking LiNKtrend's shared governance or QA standards for speed alone.

## 6. Users and Personas

- Internal LiNKtrend bots, departments, and workflows from day one.
- External agencies, operators, and developer teams that need governed skills.
- SMB and enterprise customers who want package-level logic access rather than raw skill internals.

## 7. Primary Use Cases

- Internal skill and tool registry.
- Atomic skills exposed through API and MCP.
- Department bundles and managed logic packages.
- Future enterprise entitlement, support, and telemetry layer.

## 8. Functional Requirements

- LiNKskills must have a clearly defined offer and delivery workflow.
- LiNKskills must integrate with the shared LiNKtrend operating stack where relevant.
- LiNKskills must support measurable quality and financial controls.
- LiNKskills must have documentation sufficient for repeatable delivery and troubleshooting.
- LiNKskills must support go or no-go reviews based on evidence, not intuition alone.

Line-specific workflow requirements:

- Identify required capability from internal departments or client use cases.
- Author or refine the skill and supporting tool wrappers.
- Validate using quality and policy gates.
- Register and expose to internal bots.
- Collect telemetry and improve.
- Package and expose externally once hardened.

## 9. Non-Functional Requirements

- Reliability appropriate to the commercial promise being made.
- Security and least-privilege access for production systems and credentials.
- Observability sufficient to diagnose failures without guesswork.
- Maintainability through templates, standards, and shared documentation.
- Scalability only to the degree justified by actual adoption.

## 10. Architecture and Integrations

- Governed skill registry and SOPs.
- Future API-first and MCP-accessible server layer.
- Supabase for auth, database, storage, and tenancy enforcement.
- DigitalOcean-hosted service layer.
- Progressive disclosure and run-scoped execution fragments rather than full source distribution by default.

Shared integration expectations:

- Use LiNKskills where governed logic is required.
- Use LiNKautowork where recurring process execution is required.
- Use LiNKbots where agent orchestration or digital labor is required.
- Use DigitalOcean as the default hosting base unless a clear reason exists to break that rule.

## 11. Data, Security, and Compliance

- Protect credentials, tenant data, and internal logic using centralized controls.
- Separate internal and client data where both exist.
- Document access assumptions, retention needs, and incident paths.
- Review regional and industry requirements before scaling into more sensitive workflows or markets.

## 12. Current and Future Development Needed

- LiNKskills Logic Engine gateway and entitlement layer.
- Public catalog and package browser.
- Billing, API key generation, and tenant support portal.
- Progressive-disclosure controls and telemetry.
- SDKs, MCP adapters, and package-level governance.

## 13. Roadmap Phases

Phase 1:

- define scope and minimum viable operating model
- ship the first usable version or service path
- collect real operational data

Phase 2:

- remove the highest-friction delivery bottlenecks
- improve economics through reuse and automation
- expand to the next most logical market or package layer

Phase 3:

- scale selectively based on conversion, retention, and margin
- add deeper productization or platform features only where justified
- capture a stronger strategic moat for the studio

## 14. Acceptance Criteria

- The line can be explained, sold, delivered, and supported using documented workflows.
- The line has measurable KPIs for quality, revenue, and support burden.
- The line can be run without relying on undocumented founder memory.
- The line fits LiNKtrend's wider architecture and financial logic.

## 15. Open Questions

- Which scope elements should remain internal-only versus customer-facing?
- Which features or packages deserve investment first based on margin and strategic leverage?
- What regional or vertical localization work is essential for the first scaled rollout?
- What must be automated next to preserve the factory model as demand grows?
