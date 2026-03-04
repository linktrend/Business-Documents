# 20260304 LiNKsites PRD

Status: Draft for review  
Business line: LiNKsites  
Document type: Product Requirements Document  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Product Overview

LiNKsites is a website factory for prebuilt, transferable, multi-tenant sites that convert fast and upsell into automation and bots.

## 2. Background and Current State

- Primary workspace exists at `/Users/linktrend/Projects/Dev_Sites`.
- The current system already includes a central Payload CMS, shared Next.js frontend platform, template modules, factory scripts, pricing SOPs, runbooks, and deployment guides.
- This is the most launch-ready short-term cash flow line in the portfolio.

Current development needs:

- The core multi-tenant architecture is already defined and substantially implemented.
- The biggest needs are sales tooling, template coverage, deployment polish, and smoother transfer workflows.
- The product line now needs more business packaging than fundamental architecture work.

## 3. Problem Statement

Most SMBs have weak websites, poor conversion paths, and fragmented vendors. Traditional agencies are too slow and too expensive for LiNKtrend's target customers.

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

- SMB service businesses in the US, UK, Taiwan, and Costa Rica.
- Businesses with weak digital presence and obvious conversion gaps.
- Clients that can start with a website and then expand into automations and bots.

## 7. Primary Use Cases

- Standard managed site on shared infrastructure.
- Premium site with dedicated frontend deployment.
- Add-on localization, content operations, analytics, and connected automations.

## 8. Functional Requirements

- LiNKsites must have a clearly defined offer and delivery workflow.
- LiNKsites must integrate with the shared LiNKtrend operating stack where relevant.
- LiNKsites must support measurable quality and financial controls.
- LiNKsites must have documentation sufficient for repeatable delivery and troubleshooting.
- LiNKsites must support go or no-go reviews based on evidence, not intuition alone.

Line-specific workflow requirements:

- Prospect identification by market and niche.
- Prebuilt site creation and internal QA.
- Sales outreach with a finished site already in hand.
- Close, domain mapping, transfer, and go-live.
- Managed hosting, light maintenance, and upsell path into LiNKautowork and LiNKbots.

## 9. Non-Functional Requirements

- Reliability appropriate to the commercial promise being made.
- Security and least-privilege access for production systems and credentials.
- Observability sufficient to diagnose failures without guesswork.
- Maintainability through templates, standards, and shared documentation.
- Scalability only to the degree justified by actual adoption.

## 10. Architecture and Integrations

- Next.js frontend templates.
- Payload CMS as central content and tenant control plane.
- Supabase-hosted PostgreSQL for core data storage.
- DigitalOcean-hosted shared and premium deployments.
- Optional n8n hooks for content and operational workflows.

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

- Automated lead-to-prebuild pipeline.
- Template catalog expansion by region and industry.
- More automated domain transfer and premium deployment provisioning.
- Stronger analytics and conversion benchmarking by niche.

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
