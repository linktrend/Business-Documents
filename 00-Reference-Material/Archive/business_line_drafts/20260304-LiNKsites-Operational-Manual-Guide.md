# 20260304 LiNKsites Operational Manual Guide

Status: Draft for review  
Business line: LiNKsites  
Document type: Operational Manual and Guide  
Planning basis: Updated to approved package architecture and operating mechanics.

## 1. Purpose and Scope

This manual defines how LiNKsites is operated day to day, including site factory execution, lead flow, package delivery, support handling, and troubleshooting.

## 2. What LiNKsites Is

LiNKsites is a template-first website factory that sells bundled outcomes:

- pre-built website delivery,
- managed hosting and maintenance,
- optional automation and service allowances by package.

## 3. Operating Context

- Primary workspace: `/Users/linktrend/Projects/Dev_Sites`.
- Core assets: shared Next.js frontend, central Payload CMS, factory scripts, runbooks, deployment guides.
- Hosting baseline: DigitalOcean runtime with Supabase-backed data services.
- Locale strategy: launch one locale (US or Japan), open second locale after 20 active sites in first locale.

## 4. Roles and Responsibilities

- Executive owner: pricing, scope, kill/scale decisions.
- Line lead: day-to-day execution, quality, and KPI ownership.
- QA lead: release gates and defect prevention.
- Ops lead: hosting, domain, backups, incidents, and rollback.
- Sales lead: package fit, close process, and renewal discipline.
- LiNKbot operators: maintain bot playbooks and approval policies.

## 5. Systems and Tooling

- Next.js template system for site generation.
- Payload CMS as multi-tenant content and control layer.
- Supabase for shared data services and governance controls.
- DigitalOcean for control-plane and runtime deployment.
- CRM for lead and pipeline management.
- LiNKbots for lead research, prebuild orchestration, CRM updates, and follow-up workflow triggers.
- LiNKautowork services for package allowances and post-sale automations.

## 6. Package Operations

Standard operations profile:

- no-blog lightweight site profile,
- shared runtime delivery,
- recurring price: $14.99 (1-year) or $11.99 effective (2-year),
- setup: $300.

Premium operations profile:

- richer site with blog and increased page/media envelope,
- shared runtime with higher service allowance,
- recurring price: $29.99 (1-year) or $24.99 effective (2-year),
- setup: $750,
- included allowances: 300 automations/month, 150 AI responses/month, 2 blog posts/quarter.

Enterprise operations profile:

- dedicated runtime isolation and priority service,
- recurring price: $249.99 (1-year) or $199.99 effective (2-year),
- setup: $1,999,
- domain included (costed at average $15/year),
- included allowances: 1,500 automations/month, 500 AI responses/month, 6 blog posts/quarter, on-site chat support operations.

## 7. Standard Operating Workflow

1. LiNKbot lead research and qualification.
2. Lead enrichment and insertion into CRM.
3. Template selection and prebuild generation.
4. Internal QA and package fit validation.
5. Outreach and close (human or LiNKbot-assisted process).
6. Domain mapping, go-live, and package provisioning.
7. Ongoing support, allowance tracking, and upsell monitoring.

## 8. Quality Control and Release Criteria

Minimum release gate:

- package scope validated against signed offer,
- functional checks and content checks completed,
- DNS/domain mapping validated,
- rollback plan documented,
- support handoff notes complete.

## 9. Overage and Capacity Policy Operations

Core overage rates:

- outbound transfer: $0.013/GiB,
- DB egress: $0.117/GB,
- DB size: $0.1625/GB-month,
- DB storage: $0.0273/GB-month,
- DB MAU where applicable: $0.004225/MAU-month.

Service overage rates:

- Premium: automations $0.010/execution, AI responses $0.008/response, extra blog posts $24/post.
- Enterprise: automations $0.008/execution, AI responses $0.006/response, extra blog posts $20/post.

Capacity events:

- CPU/RAM pressure is handled as a capacity event, not unit overage.
- If sustained pressure requires resize or migration, apply incremental provider cost plus 30% prorated until package alignment.

## 10. Troubleshooting and Incident Response

Incident checklist:

1. classify issue as content, template, integration, infrastructure, or capacity.
2. verify change history and recent deployments.
3. isolate impacted tenants and package tier.
4. apply rollback or containment if customer impact is material.
5. document root cause and preventive action.

Common incident classes:

- domain mapping errors,
- deployment/environment drift,
- automation allowance misconfiguration,
- provider or API dependency failures,
- capacity events from traffic spikes or heavy workflows.

## 11. Security and Data Handling Rules

- enforce least privilege for credentials and service keys,
- separate customer and internal operational contexts,
- log all material access exceptions and incidents,
- review regional legal/data implications before locale expansion.

## 12. KPI and Reporting Rules

- prebuilt sites/week,
- outreach-to-close ratio,
- setup revenue collected,
- package mix,
- recurring margin by package,
- churn by package,
- overage recovery rate,
- capacity-event count and resolution time.

## 13. Continuous Improvement Backlog

- improve lead-to-prebuild automation quality,
- expand high-converting templates by niche,
- tighten pricing/allowance fit based on real usage,
- reduce manual support load with workflow automation and better documentation.
