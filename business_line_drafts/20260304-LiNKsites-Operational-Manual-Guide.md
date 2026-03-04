# 20260304 LiNKsites Operational Manual Guide

Status: Draft for review  
Business line: LiNKsites  
Document type: Operational Manual and Guide  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Purpose and Scope

This document explains what LiNKsites is, how it operates, how it should be run day to day, how quality is protected, how issues are diagnosed, and what must be improved over time.

## 2. What It Is

LiNKsites is a website factory for prebuilt, transferable, multi-tenant sites that convert fast and upsell into automation and bots.

Mission:

Turn repeatable website delivery into immediate cash flow by building fully ready sites before the sale and transferring them into managed production quickly.

## 3. Current Operating Context

- Primary workspace exists at `/Users/linktrend/Projects/Dev_Sites`.
- The current system already includes a central Payload CMS, shared Next.js frontend platform, template modules, factory scripts, pricing SOPs, runbooks, and deployment guides.
- This is the most launch-ready short-term cash flow line in the portfolio.

## 4. Roles and Responsibilities

Core roles for this business line:

- Founder or executive owner: approves major priorities, budgets, pricing, and kill or scale decisions.
- Department owner or line lead: owns execution quality, backlog, and KPI attainment.
- QA owner: verifies release readiness and checks for avoidable defects or regressions.
- Operations owner: manages hosting, support, credentials, and incident handling.
- Media and growth owner: aligns distribution and sales support with current priorities.

## 5. Systems and Tooling

- Next.js frontend templates.
- Payload CMS as central content and tenant control plane.
- Supabase-hosted PostgreSQL for core data storage.
- DigitalOcean-hosted shared and premium deployments.
- Optional n8n hooks for content and operational workflows.

Shared system expectations:

- all production changes must be documented and reviewable
- credentials and sensitive context must be controlled centrally
- repeatable work should be automated or templatized quickly
- release and deployment actions must have rollback paths

## 6. Standard Operating Workflows

Standard workflow sequence:

1. Prospect identification by market and niche.
2. Prebuilt site creation and internal QA.
3. Sales outreach with a finished site already in hand.
4. Close, domain mapping, transfer, and go-live.
5. Managed hosting, light maintenance, and upsell path into LiNKautowork and LiNKbots.

Operational rules:

- Do not start work that cannot be tied to a clear commercial, operational, or product objective.
- Prefer template adaptation and governed reuse over net-new build paths.
- Record assumptions, credentials required, dependencies, and release notes before go-live.
- Review output quality before external delivery or production exposure.

## 7. Quality Control and Release Criteria

Minimum release criteria:

- core functionality is verified against the intended use case
- failure paths or exception handling have been tested
- support owner can diagnose common issues without reverse engineering the system
- documentation and operating notes are current
- financial and support impact of the release is understood

## 8. Troubleshooting and Incident Response

First-response troubleshooting checklist:

1. Confirm what changed, when it changed, and whether the issue is isolated or systemic.
2. Check infrastructure health, credentials, integrations, and recent deployments.
3. Reproduce the issue in the smallest possible scope.
4. Determine whether the problem is data, logic, environment, dependency, or user-flow related.
5. Apply rollback or safe-mode behavior if customer impact is material.
6. Document root cause, fix, and preventive follow-up.

Common incident classes:

- deployment or environment misconfiguration
- upstream provider or API change
- credential or permission failure
- broken template or workflow logic
- unexpected support load or user misuse
- cost spike caused by runaway compute, model use, or automation volume

## 9. Security, Data, and Compliance Rules

- Use least-privilege credentials and avoid broad shared secrets where possible.
- Separate internal and client context when the business line serves both.
- Do not expose internal logic, data, or templates unnecessarily.
- Log commercially material incidents, policy exceptions, and access issues.
- Review legal and data-handling requirements before expanding to new regions or verticals.

## 10. Maintenance and Continuous Improvement

Continuous-improvement loop:

1. Capture recurring friction, support burden, delivery delays, and quality failures.
2. Convert repeated fixes into templates, automation, or product rules.
3. Review KPI performance weekly and strategy monthly.
4. Retire, redesign, or reprice work that repeatedly breaks margin or quality expectations.

## 11. Operating KPIs

- Prebuilt sites created per week.
- Outreach to close ratio.
- Setup fees collected.
- Monthly churn.
- Upgrade rate into automation or premium hosting.
- Average gross margin per site.

## 12. Known Constraints and Open Issues

Current constraints:

- The core multi-tenant architecture is already defined and substantially implemented.
- The biggest needs are sales tooling, template coverage, deployment polish, and smoother transfer workflows.
- The product line now needs more business packaging than fundamental architecture work.

Future improvements needed:

- Automated lead-to-prebuild pipeline.
- Template catalog expansion by region and industry.
- More automated domain transfer and premium deployment provisioning.
- Stronger analytics and conversion benchmarking by niche.
