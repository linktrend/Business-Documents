# 20260304 LiNKbots PRD

Status: Draft for review  
Business line: LiNKbots  
Document type: Product Requirements Document  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Product Overview

LiNKbots is internal and client bot operating layer built on a new openclaw plus agent zero architecture with linkskills and linkautowork at the core.

## 2. Background and Current State

- The operating assumption is that the internal platform will be built in a new repo aligned to the final architecture.
- The existing LiNKbot repo is valuable as a knowledge base, deployment reference, and client-template reference, but not as the final internal architecture.
- The future model separates internal platform concerns from client deployment concerns.

Current development needs:

- The platform architecture direction is clear, but the final internal repo does not yet exist.
- The current reference material covers deployment, OpenClaw configuration, skills, and cost analysis, which is useful for the first implementation wave.

## 3. Problem Statement

Most agent deployments are either fragile experiments or oversold custom projects. LiNKbots needs a governed architecture, clear role boundaries, reusable templates, and measurable economics so bots produce operating leverage instead of support chaos.

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

- Internal LiNKtrend departments, especially COO, sites factory, app factory, QA, finance, and media functions.
- SMB clients who need recurring digital workers rather than standalone software.
- Clients buying a bundle of website, automation, and bot services together.

## 7. Primary Use Cases

- Internal head bots and worker bots.
- Client-facing managed digital workers.
- Higher-touch managed bot plus automation bundles.
- Template-based channel-integrated agents for communication or execution-heavy roles.

## 8. Functional Requirements

- LiNKbots must have a clearly defined offer and delivery workflow.
- LiNKbots must integrate with the shared LiNKtrend operating stack where relevant.
- LiNKbots must support measurable quality and financial controls.
- LiNKbots must have documentation sufficient for repeatable delivery and troubleshooting.
- LiNKbots must support go or no-go reviews based on evidence, not intuition alone.

Line-specific workflow requirements:

- Define role and department objective.
- Select runtime template and assign skills and workflows.
- Configure channels, credentials, approvals, and escalation paths.
- Test end-to-end behavior and failure handling.
- Deploy, observe, improve, and re-score economics monthly.

## 9. Non-Functional Requirements

- Reliability appropriate to the commercial promise being made.
- Security and least-privilege access for production systems and credentials.
- Observability sufficient to diagnose failures without guesswork.
- Maintainability through templates, standards, and shared documentation.
- Scalability only to the degree justified by actual adoption.

## 10. Architecture and Integrations

- New polyglot Turborepo monorepo for the internal platform.
- OpenClaw for head bots and communication-heavy workers.
- Agent Zero for execution-heavy workers.
- LiNKskills for governed skills and package access.
- LiNKautowork for repeatable process execution and handoffs.
- DigitalOcean-hosted bot infrastructure with local compute options where justified.

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

- New internal monorepo and template system.
- Identity, role, and department policy framework.
- Central telemetry and cost budget enforcement.
- Client provisioning automation and isolated deployment paths.
- Escalation, approval, and QA policy engine.

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
