# 20260304 LiNKautowork Business Plan

Status: Draft for review  
Business line: LiNKautowork  
Document type: Business Plan  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Executive Summary

LiNKautowork is a managed n8n automation line that turns internal studio workflows and industry best-practice processes into repeatable service products.

The purpose of this business line is to use internal-first automation templates and industry workflow research to create a low-cost, repeatable automation service that feels custom while remaining productized.

This business line matters to LiNKtrend because it contributes to three outcomes at once:

- it strengthens the studio's reusable production system
- it creates a direct revenue line or increases revenue per client
- it improves the economics and repeatability of the wider venture studio

## 2. Business Definition

SMBs often know they have repetitive admin and coordination pain, but they do not know how to design, test, secure, and maintain reliable automations. Agencies often overscope these builds and turn them into expensive custom projects.

Primary customer groups:

- Internal LiNKtrend departments that need automations before external sale.
- SMBs in target verticals such as dentists, restaurants, accountants, legal-adjacent services, and local operators.
- LiNKsites customers who need workflow automation after the website sale.

Primary offers:

- Starter managed automation service for one or two workflows.
- Growth automation stacks by industry.
- Localized industry best-practice automation bundles.
- Ongoing managed maintenance and exception support.

## 3. Current State

- There is not yet a dedicated LiNKautowork repo, but the product path is clear.
- LiNKsites documents already reference n8n workflows and text pipelines.
- LiNKapps starter docs already include n8n in the application environment.
- LiNKskills already includes tools and workflow-architect capability that can power this line.

## 4. Value Proposition

The core value proposition for LiNKautowork is:

Use internal-first automation templates and industry workflow research to create a low-cost, repeatable automation service that feels custom while remaining productized.

The practical advantages are:

- lower operating cost than traditional labor-heavy alternatives where reuse is possible
- faster deployment because the business line is built on reusable infrastructure and governed documentation
- stronger quality control because it is tied to LiNKtrend's shared QA, skills, and automation systems
- better upsell and cross-sell potential into adjacent business lines

## 5. Market and Customer Strategy

LiNKautowork launch strategy is internal-first:

- first 30 days: phase 1 automations for LiNKtrend internal operations and CEO execution support
- days 31 to 90: phase 2 automations for LiNKtrend Media and LiNKsites content operations
- after internal hardening and KPI validation: phase 3 commercialization into external SMB workflow bundles

Customer selection criteria:

- the customer problem must be concrete and expensive enough to justify action
- the business line must be able to deliver with limited customization
- the customer should ideally create a path to recurring revenue, upsell, or reusable insight
- the work should strengthen LiNKtrend's reusable asset base, not just generate one-off output

## 6. Delivery and Operating Model

Core build and hardening workflow:

- Map the internal or client workflow and define the target future-state process.
- Research best-practice workflows by industry.
- Source closest matching community or official base templates.
- Modify and harden workflows to LiNKtrend standards.
- Run reliability, exception-path, and credential tests.
- Deploy as a managed service and monitor execution.

Initial throughput planning assumption:

- build or refactor workflow: about 30 minutes
- QA and failure-path checks: about 30 minutes
- production hardening in internal use: about 2 to 3 weeks before broad external sale

Technology and infrastructure base:

- Self-hosted n8n on DigitalOcean-hosted infrastructure.
- JSON-based workflow templates and import pipelines.
- Credential handling via vaulting, environment isolation, and controlled support flows.
- LiNKskills orchestration for workflow design and QA.
- Event-driven triggers, webhooks, cron, and API integrations.

## 7. Business Model and Revenue Streams

Revenue logic:

- Shared credit economy with LiNKskills so one credit currency can be used across both lines.
- Recurring bundle subscriptions plus PAYG top-ups.
- Optional implementation fees for unusual integration complexity.
- Bundled upsells from LiNKsites and LiNKbots and direct standalone sales.

Pricing and packaging principles:

- Internal COGS baseline: $0.012 per credit.
- Standard: 2,500 credits at $199.99 per month (about $0.080 per credit, about 85.0% gross margin).
- Premium: 10,000 credits at $699.99 per month (about $0.070 per credit, about 82.9% gross margin).
- Enterprise: 25,000 credits at $1,624.99 per month (about $0.065 per credit, about 81.5% gross margin).
- PAYG: $0.10 per credit (about 88.0% gross margin).
- Margin floor: no package or custom statement of work can be approved below 80% gross margin without explicit executive exception.

Credit charging logic:

- every run is billed as execution credits plus tool credits
- tool credits are computed from direct provider costs with reliability buffer to prevent margin leakage
- bundle overages are charged at the client's package-effective credit rate, and no-bundle overages are charged at PAYG rate

## 8. Dependencies and Shared Services

This business line depends on shared LiNKtrend systems:

- LiNKskills for governed logic, skills, and standards where relevant
- n8n runtime and workflow library governance for recurring process execution
- LiNKbots where agent execution or support workflows matter
- QA for release and delivery control
- Admin, finance, legal, and reporting for commercial governance
- LiNKtrend Media for distribution, content, and demand generation

## 9. Key Risks and Mitigations

- Workflows breaking because of third-party API changes.
- Selling custom work under productized pricing.
- Weak monitoring causing hidden support cost.
- Credential sprawl and poor security discipline.

Mitigation principles:

- protect reuse and reject avoidable custom work
- instrument cost, quality, and delivery time from the start
- use phased rollouts and clear go or no-go gates
- treat support burden as a strategic metric, not a hidden cost

## 10. 12-Month Objectives and KPIs

Year-one objectives:

- Build and QA the first 12 phase-1 and phase-2 automations inside 30 days and place them into internal production hardening.
- Publish the first external credit-priced automation catalog within 90 days.
- Reach 10 or more recurring automation customers within 12 months.

Core KPIs:

- Internal workflows standardized.
- External workflow packages published.
- Workflow success rate.
- Time to diagnose failed runs.
- Automation upsell rate from LiNKsites.
- Credits sold by tier.
- Blended gross margin per credit.
- Gross margin by automation package.

## 11. Management Recommendation

LiNKautowork should be managed as a productized business line, not as ad hoc service work. The correct operating standard is to use shared infrastructure, keep scope tight, capture every reusable improvement back into LiNKtrend's system, and review performance against recurring revenue, margin, support burden, and strategic leverage.
