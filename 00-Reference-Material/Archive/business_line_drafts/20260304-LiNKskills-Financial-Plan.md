# 20260304 LiNKskills Financial Plan

Status: Draft for review  
Business line: LiNKskills  
Document type: Financial Plan  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Financial Purpose

The purpose of this document is to define how LiNKskills should make money, what it should cost to operate, how it should be budgeted, what its growth targets are, and what financial controls should govern scale decisions.

## 2. Revenue Strategy

- Internal leverage first.
- Pilot API subscriptions for selected skills.
- Department bundles and managed logic packages.
- Usage-based or entitlement-based contracts later.

Revenue design rules:

- Prefer recurring revenue where possible.
- Use one-time setup or transfer fees to recover launch and onboarding effort.
- Keep pricing aligned to customer value, not just internal cost.
- Avoid low-margin work that blocks reuse or forces ongoing manual intervention.

## 3. Pricing and Packaging

- Pilot API access planning anchor: about USD 99 to 299 per month.
- Department bundle planning anchor: about USD 299 to 999 or more per month.
- Managed enterprise logic-layer pricing should be custom based on entitlements, support, and telemetry needs.

Packaging principles:

- Use a small number of default packages first.
- Treat custom work as a separate pricing path, not as an entitlement inside standard packages.
- Review pricing quarterly against margin, conversion rate, and support cost.

## 4. Startup and Capital Needs

- Startup cost is mainly productization work: auth, tenancy, gateway, billing, and support tooling.
- Because the skills are already needed internally, much of the cost is dual-purpose investment rather than speculative R and D.

Funding logic:

- Use the lowest capital path that still allows reliable delivery.
- Favor shared infrastructure when it does not compromise security or quality.
- Do not front-load scale costs before demand is proven.

## 5. Operating Cost Structure

- API and orchestration hosting.
- Storage and telemetry.
- Support and package maintenance.
- Billing, key management, and documentation maintenance.

Cost-control rules:

- Track fixed and variable costs separately.
- Set budget thresholds for compute, model spend, hosting, support, and maintenance.
- Tie any major recurring spend increase to a revenue or quality justification.

## 6. Unit Economics and Margin Logic

Unit-economics expectations for LiNKskills:

- Every offer should have a defined setup effort, recurring support burden, and expected gross margin.
- High-reuse offers should expand margin over time as templates, skills, and automations improve.
- Offers that remain labor-intensive should be repriced, restructured, or retired.

## 7. 12-Month Base Case Targets

- Expose the first operational service layer internally immediately.
- Use internal bots as the first hardening loop inside the first 30 to 60 days.
- Open paid external pilot access within 90 days.
- Reach at least a handful of external paying customers within 12 months while preserving internal governance quality.

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

- Internal bot adoption.
- Number of skills and bundles exposed internally.
- Time from capability request to deployable skill.
- External pilot readiness and customer count.
- Version drift reduction across internal bots.

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

- Building the platform too slowly and missing the monetization window.
- Exposing too much source logic externally.
- Weak tenant isolation or support workflows.
- Underestimating internal demand while designing for external users.

Trigger points:

- Pause or reprice any package with persistent low or negative gross margin.
- Pause scaling if support burden rises faster than recurring revenue.
- Review product fit immediately if conversion is low despite a clear offer and active outreach.
- Kill or redesign lines that cannot be standardized enough to fit LiNKtrend's model.
