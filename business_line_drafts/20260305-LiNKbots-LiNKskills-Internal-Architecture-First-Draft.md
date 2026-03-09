# 20260305 LiNKbots LiNKskills Internal Architecture First Draft

Status: Draft for review  
Scope: internal operating architecture for LiNKtrend Venture Studio

## 1. Design Basis

This draft applies three design rules:

- each business line has one OpenClaw head bot for orchestration, governance, and cross-system reasoning
- worker bots are Agent Zero by default for focused, low-overhead execution
- deterministic repeatable workflows are pushed into n8n (LiNKautowork) rather than implemented as free-form reasoning tasks

This aligns with:

- OpenClaw strengths in multi-model orchestration and large skill ecosystems
- Agent Zero strengths in modular autonomous worker execution
- n8n strengths in deterministic triggered workflows and queue-based execution

## 2. Step 1: Bot Type by Business Line

### 2.1 Venture Studio Executive Layer

- `COO-Head` (OpenClaw): cross-line prioritization, escalation, and daily operations orchestration.
- `Ops-Worker` (Agent Zero): prepares KPI snapshots, issue queues, and execution follow-ups.

### 2.2 LiNKsites

- `LiNKsites-Head` (OpenClaw): controls intake-to-delivery pipeline, commercial packaging, and quality gates.
- `Site-Factory-Worker` (Agent Zero): clones template, configures site, prepares content mapping.
- `CMS-Worker` (Agent Zero): runs CMS updates, publishing checks, schema-safe edits.
- `Hosting-Worker` (Agent Zero): domain attach, TLS validation, runtime health checks.
- `Sales-CRM-Worker` (Agent Zero): lead qualification handoff and pipeline updates.

### 2.3 LiNKapps

- `LiNKapps-Head` (OpenClaw): PRD-to-launch orchestration and kill/hold/scale gates.
- `App-Builder-Worker` (Agent Zero): milestone implementation and integration tasks.
- `App-QA-Worker` (Agent Zero): test execution, regression checks, release gating.
- `App-Growth-Worker` (Agent Zero): onboarding instrumentation and early retention checks.

### 2.4 LiNKautowork

- `LiNKautowork-Head` (OpenClaw): automation portfolio ownership, margin control, phase sequencing.
- `Workflow-Builder-Worker` (Agent Zero): template adaptation and workflow assembly.
- `Workflow-QA-Worker` (Agent Zero): failure-path testing, retry policy checks, runbook updates.
- `Workflow-ClientOps-Worker` (Agent Zero): onboarding mappings, credential checklist, activation support.

### 2.5 LiNKskills

- `LiNKskills-Head` (OpenClaw): catalog governance, version policy, package exposure decisions.
- `Skill-Builder-Worker` (Agent Zero): create/refine skill contracts and references.
- `Tool-Builder-Worker` (Agent Zero): build and harden CLI/API wrappers.
- `Registry-QA-Worker` (Agent Zero): validation, changelog checks, publish readiness.

### 2.6 LiNKbots (Client Bot Product Line)

- `LiNKbots-Head` (OpenClaw): client bot solution architecture and package governance.
- `Bot-Provisioning-Worker` (Agent Zero): instantiate client bot from template repo baseline.
- `Bot-Integration-Worker` (Agent Zero): connector setup to LiNKskills and LiNKautowork.
- `Bot-Support-Worker` (Agent Zero): monitor health, incident triage, response SOP execution.

### 2.7 LiNKtrend Media (Exception: Additional OpenClaw Worker)

- `Media-Head` (OpenClaw): channel strategy, campaign orchestration, performance review.
- `Creative-Director-Worker` (OpenClaw): high-context creative direction, campaign narrative, multi-asset brief generation.
- `ContentOps-Worker` (Agent Zero): transforms approved briefs into execution artifacts.
- `Distribution-Worker` (Agent Zero): schedule/publish/report loops and channel operations.

Rationale for exception:

- creative strategic synthesis benefits from a second high-capability OpenClaw worker in this line
- repetitive channel execution remains in Agent Zero plus n8n workflows

## 3. Step 2: Task Definition by Business Line

## 3.1 Venture Studio Executive Layer Tasks

- generate daily 08:00 briefing: wins, blockers, financial health, top decisions
- monitor cross-line KPIs and trigger escalations
- enforce weekly operating cadence and priority updates
- coordinate resource shifts across LiNKsites, LiNKautowork, and LiNKskills

Deterministic tasks for n8n:

- daily data aggregation and briefing payload assembly
- KPI snapshot extraction from CRM, finance, and run logs
- recurring reminder and follow-up workflows

## 3.2 LiNKsites Tasks

- lead intake and qualification for prebuilt site offers
- demo-site generation and delivery tracking
- CMS content publish workflow
- domain attachment and go-live checklist execution
- post-launch monitoring, incident response, and overage flags

Deterministic tasks for n8n:

- inbound lead ingestion, scoring, and CRM sync
- contact form routing and autoresponder sequences
- content sync and scheduled publishing
- uptime/health alerts and ticket creation

## 3.3 LiNKapps Tasks

- PRD decomposition into milestones and acceptance criteria
- implementation scheduling and dependency tracking
- test orchestration and deployment-gate checks
- usage and billing instrumentation checks
- launch review and kill/hold/scale evidence package generation

Deterministic tasks for n8n:

- CI event-to-alert routing
- usage and billing event pipeline normalization
- release checklist automation and gate reminders

## 3.4 LiNKautowork Tasks

- select highest-value internal workflows and source nearest templates
- adapt workflows to LiNKtrend standards and run QA gates
- monitor run success rate, retries, and exception patterns
- package validated workflows as external catalog offers
- enforce credit-cost discipline and margin thresholds

Deterministic tasks for n8n:

- workflow execution itself
- retry logic, dead-letter alerts, and incident routing
- usage metering events to billing

## 3.5 LiNKskills Tasks

- define skill contracts and package boundaries
- wrap tools for deterministic access control and telemetry
- maintain versioned registry and publish controls
- expose internal-first packages for bot operations
- prepare external API/MCP productization

Deterministic tasks for n8n:

- release pipeline notifications
- registry publish checklists
- usage telemetry fanout to analytics and billing

## 3.6 LiNKbots Tasks

- convert client requirement into bot package blueprint
- provision bot instances from template baselines
- attach approved skills and automation hooks
- validate end-to-end bot behavior and handoff
- operate managed support and upgrade cadence

Deterministic tasks for n8n:

- onboarding workflow state tracking
- provisioning event notifications
- support queue routing and SLA timers

## 3.7 LiNKtrend Media Tasks

- generate monthly campaign calendar and weekly asset plan
- execute multi-channel content production and QA loop
- repurpose website content into distribution formats
- publish and monitor performance metrics
- feed performance signals back into strategy updates

Deterministic tasks for n8n:

- topic-to-asset pipeline orchestration
- scheduling and publication to channels
- post-publication analytics aggregation

## 4. Step 3: LiNKskills First Development Set

## 4.1 Priority Rule

Develop first the skills and tools that internal bots need to run LiNKtrend operations across LiNKsites, LiNKautowork, LiNKapps, LiNKbots, and Media.

## 4.2 P0 Skills (Develop or Harden First)

- `department-head`
- `executive-sync-8am`
- `studio-health-reporting`
- `repository-manager`
- `audit-protocol`
- `workflow-architect`
- `software-pm`
- `devops-sre`
- `persistent-qa`
- `marketing-strategist`
- `channel-ops`
- `creative-director`
- `creative-qa`
- `studio-controller`
- `smart-file-clerk`
- `compliance-guardian`

## 4.3 P0 Tools (Develop or Harden First)

- `n8n`
- `n8n-bridge`
- `memory`
- `vault`
- `research`
- `usage`
- `social-gw`
- `doc-engine`
- `playwright-cli`
- `sandbox`

## 4.4 P1 Skills (After P0 Stabilization)

- `market-analyst`
- `seo-semantic-auditor`
- `engagement-to-strategy-loop`
- `tool-architect`
- `skill-architect`
- `prd-architect`

## 5. n8n vs LiNKskills Decision Framework

Use n8n when the workflow is:

- trigger-driven and deterministic
- integration-heavy and repetitive
- required to run at fixed schedules or event hooks
- easier to audit as state transitions than as model reasoning

Use LiNKskills when the task is:

- policy-heavy and judgment-based
- ambiguous and requires adaptive reasoning
- a cross-tool orchestration decision, not just execution
- a reusable intelligence contract that should be governed and versioned

Use both when:

- a skill decides plan/policy and n8n executes deterministic steps
- a head bot supervises outcomes while n8n handles run mechanics

## 6. Phase 1 and Phase 2 Automation Program (Initial 12)

## 6.1 Phase 1 (Internal Operations First)

1. lead capture, enrichment, and CRM routing  
2. inbox triage and response drafting  
3. meeting scheduling and calendar conflict resolution  
4. meeting transcript to actions and follow-up orchestration  
5. receipt or invoice ingestion and accounting prep  
6. client onboarding task and timeline orchestrator  

## 6.2 Phase 2 (Media and Content Operations)

7. long-form source to website article generator  
8. topic and brief generator from niche and offer inputs  
9. brand and compliance QA pre-publish check  
10. post-publish analytics capture and weekly report  
11. multi-channel native publishing pipeline  
12. content scheduler and queue manager

## 7. Proposed Launch Sequence

- Week 1: finalize head-bot topology, worker roles, and P0 skill/tool contracts
- Week 2: ship first 6 phase-1 automations and begin internal hardening
- Week 3: ship remaining 6 phase-2 automations and integrate dashboard controls
- Week 4: publish internal runbooks, KPI dashboard, and external commercialization readiness checklist

## 8. Open Decisions for Next Revision

- final naming conventions for each head and worker bot instance
- exact CRM target and data model for lead and customer lifecycle
- first public automation catalog scope for SMB vertical rollout
- first LiNKskills package SKUs and credit pricing by package depth
