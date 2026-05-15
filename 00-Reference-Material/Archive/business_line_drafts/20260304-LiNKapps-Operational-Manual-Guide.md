# 20260304 LiNKapps Operational Manual Guide

Status: Draft for review  
Business line: LiNKapps  
Document type: Operational Manual and Guide  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Purpose and Scope

This document explains what LiNKapps is, how it operates, how it should be run day to day, how quality is protected, how issues are diagnosed, and what must be improved over time.

## 2. What It Is

LiNKapps is an app factory and venture portfolio engine for rapid launch, validation, and either exit or long-term hold.

Mission:

Launch many low-cost, high-speed software ventures from a shared foundation so LiNKtrend can discover winners without accepting traditional startup burn.

## 3. Current Operating Context

- Primary workspace exists at `/Users/linktrend/Projects/Dev_Apps`.
- LiNKdev Starter Kit already includes Next.js, React Native, Supabase, Stripe, n8n hooks, MCP integration, and testing guidance.
- A PRD-to-independent-app workflow already exists and is suitable for repeated launches.
- The main constraint is not stack readiness; it is disciplined opportunity selection and launch focus.

## 4. Roles and Responsibilities

Core roles for this business line:

- Founder or executive owner: approves major priorities, budgets, pricing, and kill or scale decisions.
- Department owner or line lead: owns execution quality, backlog, and KPI attainment.
- QA owner: verifies release readiness and checks for avoidable defects or regressions.
- Operations owner: manages hosting, support, credentials, and incident handling.
- Media and growth owner: aligns distribution and sales support with current priorities.

## 5. Systems and Tooling

- Next.js for web applications.
- React Native and Expo for mobile when required.
- Supabase for auth, database, storage, and access controls.
- Stripe for billing and subscription management.
- n8n for workflow and background automation.
- Playwright, Vitest, and release gates for QA and deployment readiness.

Shared system expectations:

- all production changes must be documented and reviewable
- credentials and sensitive context must be controlled centrally
- repeatable work should be automated or templatized quickly
- release and deployment actions must have rollback paths

## 6. Standard Operating Workflows

Standard workflow sequence:

1. Opportunity sourcing and scoring.
2. PRD creation and founder go or no-go decision.
3. Repository generation from the starter kit.
4. Build, test, launch, and observe.
5. 30, 60, and 90 day kill, hold, or scale review.
6. Data-room preparation for sale if the asset is listed.

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

- Days from idea to PRD approval.
- Days from PRD approval to launch.
- Activation rate.
- First 30-day retention.
- MRR by app.
- Gross margin by app.
- Kill, hold, or scale decision cycle time.

## 12. Known Constraints and Open Issues

Current constraints:

- A strong starter platform exists.
- The missing pieces are portfolio governance, launch analytics discipline, and repeatable venture scoring.
- Each app still needs more explicit templates for market validation, pricing tests, and exit package preparation.

Future improvements needed:

- Automated venture scoring assistant and PRD intake pipeline.
- Launch scoreboard for acquisition, activation, retention, revenue, and support cost.
- Standard operating checklist for app sale readiness.
- Localization framework for Taiwan, Costa Rica, US, and UK launch reuse.
