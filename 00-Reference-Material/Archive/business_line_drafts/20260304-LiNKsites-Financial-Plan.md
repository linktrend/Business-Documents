# 20260304 LiNKsites Financial Plan

Status: Draft for review  
Business line: LiNKsites  
Document type: Financial Plan  
Planning basis: Updated to approved LiNKsites package pricing, cost, and margin assumptions.

## 1. Financial Purpose

Define the operating economics of LiNKsites so pricing, growth, and scaling decisions stay controlled and margin-positive.

## 2. Revenue Strategy

LiNKsites uses two revenue layers:

- one-time setup revenue from template-based site delivery,
- recurring managed-hosting and operations revenue by package.

Additional revenue layers:

- usage overages,
- scoped add-ons and service expansions,
- cross-sell into LiNKautowork and LiNKbots.

## 3. Approved Package Pricing

Standard:

- setup: $300,
- recurring: $14.99/month (1-year) or $11.99/month effective (2-year).

Premium:

- setup: $750,
- recurring: $29.99/month (1-year) or $24.99/month effective (2-year).

Enterprise:

- setup: $1,999,
- recurring: $249.99/month (1-year) or $199.99/month effective (2-year).

## 4. Cost Structure Baseline

Shared management allocation for LiNKsites:

- DigitalOcean base allocation: $7.92/month,
- weekly backup allocation: $4.80/month,
- Supabase allocation: $6.25/month,
- total management layer allocation: $18.97/month.

Recurring internal cost per site:

- Standard: $1.72/site/month,
- Premium: $4.10/site/month,
- Enterprise: about $37.30/site/month (includes average domain allowance of about $15/year).

Estimated AI token build cost per site:

- Standard: about $0.45,
- Premium: about $1.85,
- Enterprise: about $4.90.

## 5. Recurring Margin Logic

Recurring gross margin by package:

- Standard: 88.53% (1-year), 85.65% (2-year),
- Premium: 86.33% (1-year), 83.59% (2-year),
- Enterprise: 85.08% (1-year), 81.35% (2-year).

Recurring monthly gross profit per site:

- Standard: $13.27 (1-year), $10.27 (2-year),
- Premium: $25.89 (1-year), $20.89 (2-year),
- Enterprise: $212.69 (1-year), $162.69 (2-year).

## 6. Overage Economics

Core overage charges:

- outbound transfer: $0.013 per GiB,
- DB egress: $0.117 per GB,
- DB size: $0.1625 per GB-month,
- DB storage: $0.0273 per GB-month,
- DB MAU where applicable: $0.004225 per MAU-month.

Service overages:

- Premium automations: $0.010 per execution,
- Premium AI responses: $0.008 per response,
- Premium extra blog posts: $24 per post,
- Enterprise automations: $0.008 per execution,
- Enterprise AI responses: $0.006 per response,
- Enterprise extra blog posts: $20 per post.

Capacity event rule:

- CPU and RAM are not treated as unit-metered overages.
- If sustained pressure requires resize or migration, incremental provider cost plus 30% can be charged prorated until package alignment is complete.

## 7. Capital and Budget Guidance

Financial control priorities:

- protect shared reliability first (hosting, backups, QA discipline),
- treat model/API usage as measured operating spend, not uncontrolled variable cost,
- tie new recurring spend to proven customer growth and package performance.

## 8. 12-Month Financial Targets

Target outcomes:

- first 4 to 6 paying clients within 90 days,
- 20 plus active sites in first locale before second locale expansion,
- package mix that keeps blended gross margin high while preserving support quality.

Illustrative recurring contribution model:

- keep Standard as throughput and entry path,
- use Premium to increase ARPU with bounded support complexity,
- use Enterprise for high-margin dedicated service with strict scope and SLA controls.

## 9. Financial KPIs and Controls

- setup revenue collected per month,
- recurring revenue by package,
- gross margin by package,
- support burden by package,
- overage recovered versus overage incurred,
- churn and retention by package and cohort,
- payback period by acquisition source.

## 10. Reinvestment Policy

Reinvest in this order:

1. reliability and quality controls,
2. delivery automation and reusable templates,
3. sales throughput systems and CRM instrumentation,
4. locale expansion after customer-density trigger is achieved.

## 11. Risk Controls

- Reject custom work that breaks package economics.
- Reprice or tighten packages if support burden rises faster than recurring margin.
- Pause expansion if first-locale operations are unstable.
- Keep cost attribution visible by package to prevent hidden margin erosion.
