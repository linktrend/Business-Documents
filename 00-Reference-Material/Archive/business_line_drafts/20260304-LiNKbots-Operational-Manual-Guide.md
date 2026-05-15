# 20260304 LiNKbots Operational Manual Guide

Status: Draft for review  
Business line: LiNKbots  
Document type: Operational Manual and Guide  
Planning basis: This draft uses a consistent structure informed by current business-plan, SOP, financial-planning, strategy-execution, and PRD best practices, then adapts them to LiNKtrend's operating model and current repository context.

## 1. Purpose and Scope

This document explains what LiNKbots is, how it operates, how it should be run day to day, how quality is protected, how issues are diagnosed, and what must be improved over time.

## 2. What It Is

LiNKbots is internal and client bot operating layer built on a new openclaw plus agent zero architecture with linkskills and linkautowork at the core.

Mission:

Create a modular AI workforce layer that runs LiNKtrend internally and can also be provisioned into client-facing digital worker products without mixing the two product models.

## 3. Current Operating Context

- The operating assumption is that the internal platform will be built in a new repo aligned to the final architecture.
- The existing LiNKbot repo is valuable as a knowledge base, deployment reference, and client-template reference, but not as the final internal architecture.
- The future model separates internal platform concerns from client deployment concerns.

## 4. Roles and Responsibilities

Core roles for this business line:

- Founder or executive owner: approves major priorities, budgets, pricing, and kill or scale decisions.
- Department owner or line lead: owns execution quality, backlog, and KPI attainment.
- QA owner: verifies release readiness and checks for avoidable defects or regressions.
- Operations owner: manages hosting, support, credentials, and incident handling.
- Media and growth owner: aligns distribution and sales support with current priorities.

## 5. Systems and Tooling

- New polyglot Turborepo monorepo for the internal platform.
- OpenClaw for head bots and communication-heavy workers.
- Agent Zero for execution-heavy workers.
- LiNKskills for governed skills and package access.
- LiNKautowork for repeatable process execution and handoffs.
- DigitalOcean-hosted bot infrastructure with local compute options where justified.

Shared system expectations:

- all production changes must be documented and reviewable
- credentials and sensitive context must be controlled centrally
- repeatable work should be automated or templatized quickly
- release and deployment actions must have rollback paths

## 6. Standard Operating Workflows

Standard workflow sequence:

1. Define role and department objective.
2. Select runtime template and assign skills and workflows.
3. Configure channels, credentials, approvals, and escalation paths.
4. Test end-to-end behavior and failure handling.
5. Deploy, observe, improve, and re-score economics monthly.

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

- Internal task coverage by bots.
- Pilot-to-retained-client conversion.
- Average monthly revenue per bot client.
- Gross margin after compute and model spend.
- Intervention rate and incident frequency.

## 12. Known Constraints and Open Issues

Current constraints:

- The platform architecture direction is clear, but the final internal repo does not yet exist.
- The current reference material covers deployment, OpenClaw configuration, skills, and cost analysis, which is useful for the first implementation wave.

Future improvements needed:

- New internal monorepo and template system.
- Identity, role, and department policy framework.
- Central telemetry and cost budget enforcement.
- Client provisioning automation and isolated deployment paths.
- Escalation, approval, and QA policy engine.
