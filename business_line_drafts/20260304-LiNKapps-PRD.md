# 20260304 LiNKapps PRD

Status: Draft for review  
Business line: LiNKapps  
Document type: Product Requirements Document  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Product Overview

LiNKapps is an app factory and venture portfolio engine for rapid launch, validation, and either exit or long-term hold.

## 2. Background and Current State

- Primary workspace exists at `/Users/linktrend/Projects/Dev_Apps`.
- LiNKdev Starter Kit already includes Next.js, React Native, Supabase, Stripe, n8n hooks, MCP integration, and testing guidance.
- A PRD-to-independent-app workflow already exists and is suitable for repeated launches.
- The main constraint is not stack readiness; it is disciplined opportunity selection and launch focus.

Current development needs:

- A strong starter platform exists.
- The missing pieces are portfolio governance, launch analytics discipline, and repeatable venture scoring.
- Each app still needs more explicit templates for market validation, pricing tests, and exit package preparation.

## 3. Problem Statement

Traditional product studios spend too much time and salary burn on custom foundations, weak prioritization, and slow launch cycles. LiNKapps exists to reduce cycle time, standardize the build system, and make failure affordable.

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

- End users and SMB operators served by each individual app.
- Internal LiNKtrend teams that need production-grade product infrastructure quickly.
- Potential buyers on software marketplaces and direct acquirers once an app clears target KPIs.

## 7. Primary Use Cases

- Independent web and mobile applications generated from the LiNKdev Starter Kit.
- Niche SaaS products localized by market or vertical.
- Exit-ready digital assets with documented operating history, billing, telemetry, and deployment runbooks.

## 8. Functional Requirements

- LiNKapps must have a clearly defined offer and delivery workflow.
- LiNKapps must integrate with the shared LiNKtrend operating stack where relevant.
- LiNKapps must support measurable quality and financial controls.
- LiNKapps must have documentation sufficient for repeatable delivery and troubleshooting.
- LiNKapps must support go or no-go reviews based on evidence, not intuition alone.

Line-specific workflow requirements:

- Opportunity sourcing and scoring.
- PRD creation and founder go or no-go decision.
- Repository generation from the starter kit.
- Build, test, launch, and observe.
- 30, 60, and 90 day kill, hold, or scale review.
- Data-room preparation for sale if the asset is listed.

## 9. Non-Functional Requirements

- Reliability appropriate to the commercial promise being made.
- Security and least-privilege access for production systems and credentials.
- Observability sufficient to diagnose failures without guesswork.
- Maintainability through templates, standards, and shared documentation.
- Scalability only to the degree justified by actual adoption.

## 10. Architecture and Integrations

- Next.js for web applications.
- React Native and Expo for mobile when required.
- Supabase for auth, database, storage, and access controls.
- Stripe for billing and subscription management.
- n8n for workflow and background automation.
- Playwright, Vitest, and release gates for QA and deployment readiness.

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

- Automated venture scoring assistant and PRD intake pipeline.
- Launch scoreboard for acquisition, activation, retention, revenue, and support cost.
- Standard operating checklist for app sale readiness.
- Localization framework for Taiwan, Costa Rica, US, and UK launch reuse.

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
