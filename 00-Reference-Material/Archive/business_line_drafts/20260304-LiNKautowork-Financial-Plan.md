# 20260304 LiNKautowork Financial Plan

Status: Draft for review  
Business line: LiNKautowork  
Document type: Financial Plan  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Financial Purpose

The purpose of this document is to define how LiNKautowork should make money, what it should cost to operate, how it should be budgeted, what its growth targets are, and what financial controls should govern scale decisions.

## 2. Revenue Strategy

- Shared credit economy with LiNKskills.
- Recurring bundle subscriptions plus PAYG top-ups.
- Optional implementation fees for non-standard integrations.
- Bundled upsells from LiNKsites and LiNKbots.

Revenue design rules:

- Prefer recurring revenue where possible.
- Use one-time setup or transfer fees to recover launch and onboarding effort.
- Keep pricing aligned to customer value, not just internal cost.
- Avoid low-margin work that blocks reuse or forces ongoing manual intervention.

## 3. Pricing and Packaging

Approved credit pricing:

- Internal COGS baseline: $0.012 per credit.
- Standard: 2,500 credits at $199.99 per month (about $0.080 per credit, about 85.0% gross margin).
- Premium: 10,000 credits at $699.99 per month (about $0.070 per credit, about 82.9% gross margin).
- Enterprise: 25,000 credits at $1,624.99 per month (about $0.065 per credit, about 81.5% gross margin).
- PAYG: $0.10 per credit (about 88.0% gross margin).
- Minimum gross margin threshold: 80% on all published packages.

Credit metering rule:

- total billed credits = execution credits + tool credits
- tool credits scale with direct provider cost (LLM, OCR, enrichment, API calls) plus reliability buffer
- overage credits in bundles are billed at the customer's package-effective rate

Packaging principles:

- Use a small number of default packages first.
- Treat custom work as a separate pricing path, not as an entitlement inside standard packages.
- Review pricing quarterly against margin, conversion rate, and support cost.

## 4. Startup and Capital Needs

- Incremental startup cost is mainly n8n deployment, credential policy setup, workflow QA, and offer-page creation.
- Because internal workflows must be built anyway, the first product assets can double as internal operating infrastructure.
- The biggest hidden cost is unreliable workflows creating support load, so testing and monitoring must be funded from day one.

Funding logic:

- Use the lowest capital path that still allows reliable delivery.
- Favor shared infrastructure when it does not compromise security or quality.
- Do not front-load scale costs before demand is proven.

## 5. Operating Cost Structure

- n8n hosting and execution cost.
- Credential storage and monitoring overhead.
- Support time for failed runs and vendor changes.
- Ongoing template maintenance as APIs evolve.

Cost-control rules:

- Track fixed and variable costs separately.
- Set budget thresholds for compute, model spend, hosting, support, and maintenance.
- Tie any major recurring spend increase to a revenue or quality justification.

## 6. Unit Economics and Margin Logic

Unit-economics expectations for LiNKautowork:

- Every offer should have defined execution-credit and tool-credit expectations.
- Every offer should maintain at least 80% gross margin at expected volume.
- High-reuse offers should expand margin over time as templates, skills, and automations improve.
- Offers that remain labor-intensive should be repriced, restructured, or retired.

## 7. 12-Month Base Case Targets

- Build and QA the first 12 automations for phase 1 and phase 2 within 30 days and move into internal hardening.
- Publish the first external credit-priced automation catalog within 90 days.
- Reach 10 or more recurring automation customers within 12 months.

Base-case financial interpretation:

- Month 1 to 3 should focus on getting the first paying proof points and validating margin assumptions.
- Month 4 to 6 should focus on repeatability, retention, and support-cost control.
- Month 7 to 12 should focus on scaling only the offers that preserve contribution margin and strategic leverage.

## 8. Upside and Downside Scenarios

Upside case:

- conversion rates exceed plan because the value proposition is obvious and the delivery path is fast
- shared infrastructure produces better-than-expected margin
- cross-sell into other LiNKtrend services increases revenue per customer

Downside case:

- support cost rises because the product is not stable enough
- pricing is too low relative to the hidden operating burden
- the line generates revenue but weak strategic leverage because work is too custom

## 9. Budget Allocation Rules

- Protect spend on reliability, documentation, and QA before adding discretionary growth spend.
- Route discretionary investment toward the bottleneck with the highest commercial leverage.
- Do not let marketing, infrastructure, or model spend expand faster than proven unit economics.

## 10. Financial KPIs and Controls

- Internal workflows standardized.
- External workflow packages published.
- Workflow success rate.
- Time to diagnose failed runs.
- Automation upsell rate from LiNKsites.
- Credits sold by tier and PAYG share.
- Blended gross margin per credit.
- Tool-credit share versus execution-credit share.
- Gross margin by automation package.

Additional finance controls:

- monthly revenue by package or asset
- gross margin by package or asset
- support hours or support cost per customer
- hosting, model, and workflow execution cost by product line where practical
- customer acquisition source and payback period where applicable

## 11. Reinvestment Policy

Reinvestment order:

1. stabilize delivery quality and reduce failure or support cost
2. improve reuse through templates, automations, and skills
3. increase distribution only after the offer converts and retains reliably
4. expand into new markets, verticals, or product layers once the core economics are proven

## 12. Financial Risks and Trigger Points

- Workflows breaking because of third-party API changes.
- Selling custom work under productized pricing.
- Weak monitoring causing hidden support cost.
- Credential sprawl and poor security discipline.

Trigger points:

- Pause or reprice any package with persistent low or negative gross margin.
- Pause scaling if support burden rises faster than recurring revenue.
- Review product fit immediately if conversion is low despite a clear offer and active outreach.
- Kill or redesign lines that cannot be standardized enough to fit LiNKtrend's model.
