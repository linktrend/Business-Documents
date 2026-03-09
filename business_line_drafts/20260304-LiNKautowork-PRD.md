# 20260304 LiNKautowork PRD

Status: Draft for review  
Business line: LiNKautowork  
Document type: Product Requirements Document  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Product Overview

LiNKautowork is a managed n8n automation line that turns internal studio workflows and industry best-practice processes into repeatable service products.

## 2. Background and Current State

- There is not yet a dedicated LiNKautowork repo, but the product path is clear.
- LiNKsites documents already reference n8n workflows and text pipelines.
- LiNKapps starter docs already include n8n in the application environment.
- LiNKskills already includes tools and workflow-architect capability that can power this line.

Current development needs:

- The core idea is validated by internal need and existing stack references, but the product line needs its own registry, packaging, and monitoring discipline.
- The current gap is not feasibility; it is formalization into a business-ready service line.

## 3. Problem Statement

SMBs often know they have repetitive admin and coordination pain, but they do not know how to design, test, secure, and maintain reliable automations. Agencies often overscope these builds and turn them into expensive custom projects.

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

- Internal LiNKtrend departments that need automations before external sale.
- SMBs in target verticals such as dentists, restaurants, accountants, legal-adjacent services, and local operators.
- LiNKsites customers who need workflow automation after the website sale.

## 7. Primary Use Cases

- Phase 1 internal operations automations for LiNKtrend execution.
- Phase 2 content and publishing automations for LiNKtrend Media and LiNKsites support.
- Phase 3 external SMB workflow bundles by vertical.
- Ongoing managed maintenance and exception support.

## 8. Functional Requirements

- LiNKautowork must have a clearly defined offer and delivery workflow.
- LiNKautowork must integrate with the shared LiNKtrend operating stack where relevant.
- LiNKautowork must support measurable quality and financial controls.
- LiNKautowork must have documentation sufficient for repeatable delivery and troubleshooting.
- LiNKautowork must support go or no-go reviews based on evidence, not intuition alone.

Line-specific workflow requirements:

- Map the internal or client workflow and define the target future-state process.
- Research best-practice workflows by industry.
- Source closest matching community or official base templates.
- Modify and harden workflows to LiNKtrend standards.
- Run reliability, exception-path, and credential tests.
- Deploy as a managed service and monitor execution.
- Meter every run as execution credits plus tool credits.

## 9. Non-Functional Requirements

- Reliability appropriate to the commercial promise being made.
- Security and least-privilege access for production systems and credentials.
- Observability sufficient to diagnose failures without guesswork.
- Maintainability through templates, standards, and shared documentation.
- Scalability only to the degree justified by actual adoption.

## 10. Architecture and Integrations

- Self-hosted n8n on DigitalOcean-hosted infrastructure.
- JSON-based workflow templates and import pipelines.
- Credential handling via vaulting, environment isolation, and controlled support flows.
- LiNKskills orchestration for workflow design and QA.
- Event-driven triggers, webhooks, cron, and API integrations.

Shared integration expectations:

- Use LiNKskills where governed logic is required.
- Use LiNKautowork where recurring process execution is required.
- Use LiNKbots where agent orchestration or digital labor is required.
- Use DigitalOcean as the default hosting base unless a clear reason exists to break that rule.

Commercial architecture requirements:

- Use a shared credit currency with LiNKskills.
- Keep internal COGS baseline at $0.012 per credit.
- Maintain published package margin floor of at least 80%.
- Support Standard (2,500 credits), Premium (10,000 credits), Enterprise (25,000 credits), and PAYG billing.

## 11. Data, Security, and Compliance

- Protect credentials, tenant data, and internal logic using centralized controls.
- Separate internal and client data where both exist.
- Document access assumptions, retention needs, and incident paths.
- Review regional and industry requirements before scaling into more sensitive workflows or markets.

## 12. Current and Future Development Needed

- Dedicated repo and catalog for workflow templates.
- Credential and support policy framework.
- Execution logs, SLA monitoring, and failure alerting.
- Customer-facing website, intake flow, and managed onboarding path.

## 13. Roadmap Phases

Phase 1:

- build and QA first 12 automations for internal operations and CEO support
- deploy to internal production with reliability monitoring
- collect operational and cost telemetry

Phase 2:

- ship LiNKtrend Media and LiNKsites content automation set
- publish external credit-priced offers through web channels
- improve economics through tool-credit controls and template reuse

Phase 3:

- scale selectively based on conversion, retention, and margin
- expand into SMB administrative workflow verticals
- add deeper productization features only where justified by usage and margin data

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
