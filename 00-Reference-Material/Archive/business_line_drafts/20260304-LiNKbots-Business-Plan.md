# 20260304 LiNKbots Business Plan

Status: Draft for review  
Business line: LiNKbots  
Document type: Business Plan  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Executive Summary

LiNKbots is internal and client bot operating layer built on a new openclaw plus agent zero architecture with linkskills and linkautowork at the core.

The purpose of this business line is to create a modular ai workforce layer that runs linktrend internally and can also be provisioned into client-facing digital worker products without mixing the two product models.

This business line matters to LiNKtrend because it contributes to three outcomes at once:

- it strengthens the studio's reusable production system
- it creates a direct revenue line or increases revenue per client
- it improves the economics and repeatability of the wider venture studio

## 2. Business Definition

Most agent deployments are either fragile experiments or oversold custom projects. LiNKbots needs a governed architecture, clear role boundaries, reusable templates, and measurable economics so bots produce operating leverage instead of support chaos.

Primary customer groups:

- Internal LiNKtrend departments, especially COO, sites factory, app factory, QA, finance, and media functions.
- SMB clients who need recurring digital workers rather than standalone software.
- Clients buying a bundle of website, automation, and bot services together.

Primary offers:

- Internal head bots and worker bots.
- Client-facing managed digital workers.
- Higher-touch managed bot plus automation bundles.
- Template-based channel-integrated agents for communication or execution-heavy roles.

## 3. Current State

- The operating assumption is that the internal platform will be built in a new repo aligned to the final architecture.
- The existing LiNKbot repo is valuable as a knowledge base, deployment reference, and client-template reference, but not as the final internal architecture.
- The future model separates internal platform concerns from client deployment concerns.

## 4. Value Proposition

The core value proposition for LiNKbots is:

Create a modular AI workforce layer that runs LiNKtrend internally and can also be provisioned into client-facing digital worker products without mixing the two product models.

The practical advantages are:

- lower operating cost than traditional labor-heavy alternatives where reuse is possible
- faster deployment because the business line is built on reusable infrastructure and governed documentation
- stronger quality control because it is tied to LiNKtrend's shared QA, skills, and automation systems
- better upsell and cross-sell potential into adjacent business lines

## 5. Market and Customer Strategy

LiNKbots should launch with the same multi-market bias as the wider studio: the United States, United Kingdom, Taiwan, and Costa Rica.

Customer selection criteria:

- the customer problem must be concrete and expensive enough to justify action
- the business line must be able to deliver with limited customization
- the customer should ideally create a path to recurring revenue, upsell, or reusable insight
- the work should strengthen LiNKtrend's reusable asset base, not just generate one-off output

## 6. Delivery and Operating Model

Core workflows:

- Define role and department objective.
- Select runtime template and assign skills and workflows.
- Configure channels, credentials, approvals, and escalation paths.
- Test end-to-end behavior and failure handling.
- Deploy, observe, improve, and re-score economics monthly.

Technology and infrastructure base:

- New polyglot Turborepo monorepo for the internal platform.
- OpenClaw for head bots and communication-heavy workers.
- Agent Zero for execution-heavy workers.
- LiNKskills for governed skills and package access.
- LiNKautowork for repeatable process execution and handoffs.
- DigitalOcean-hosted bot infrastructure with local compute options where justified.

## 7. Business Model and Revenue Streams

Revenue logic:

- Pilot setup fees.
- Managed monthly worker fees.
- Bundled service revenue with websites and automation.
- Higher-margin recurring contracts for narrow but valuable digital labor replacements.

Pricing and packaging principles:

- Pilot planning anchor: about USD 1,000 to 2,000 one-time plus USD 1,000 to 2,000 per month.
- Managed digital worker anchor: about USD 1,500 to 3,500 one-time plus USD 1,500 to 3,500 per month.
- Managed bot plus automation stack anchor: about USD 2,500 to 5,000 one-time plus USD 3,000 to 7,000 per month.

## 8. Dependencies and Shared Services

This business line depends on shared LiNKtrend systems:

- LiNKskills for governed logic, skills, and standards where relevant
- LiNKautowork for recurring process execution and handoffs where relevant
- LiNKbots where agent execution or support workflows matter
- QA for release and delivery control
- Admin, finance, legal, and reporting for commercial governance
- LiNKtrend Media for distribution, content, and demand generation

## 9. Key Risks and Mitigations

- Overpromising digital labor before the templates are stable.
- Mixing internal and client concerns in one architecture.
- Runaway model costs.
- Weak observability causing failure to detect degraded bot behavior.

Mitigation principles:

- protect reuse and reject avoidable custom work
- instrument cost, quality, and delivery time from the start
- use phased rollouts and clear go or no-go gates
- treat support burden as a strategic metric, not a hidden cost

## 10. 12-Month Objectives and KPIs

Year-one objectives:

- Deploy the first internal department bots within 30 days of platform readiness.
- Run the first 1 to 2 client bot pilots within 90 days where scope is tightly controlled.
- Reach 4 or more profitable managed bot clients within 12 months.

Core KPIs:

- Internal task coverage by bots.
- Pilot-to-retained-client conversion.
- Average monthly revenue per bot client.
- Gross margin after compute and model spend.
- Intervention rate and incident frequency.

## 11. Management Recommendation

LiNKbots should be managed as a productized business line, not as ad hoc service work. The correct operating standard is to use shared infrastructure, keep scope tight, capture every reusable improvement back into LiNKtrend's system, and review performance against recurring revenue, margin, support burden, and strategic leverage.
