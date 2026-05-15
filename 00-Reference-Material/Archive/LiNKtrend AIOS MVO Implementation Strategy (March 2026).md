# LiNKtrend AIOS MVO Implementation Strategy (March 2026)

## 1) Document Control
- Version: `1.0`
- Date: `March 10, 2026`
- Target Go-Live: `March 15, 2026`
- Related references:
  - [LiNKtrend Autonomous Organizational Structure v2.0.md](./LiNKtrend%20Autonomous%20Organizational%20Structure%20v2.0.md)
  - [AIOS Implementation Blueprint for LiNKtrend.md](./AIOS%20Implementation%20Blueprint%20for%20LiNKtrend.md)

## 2) Objective
Establish a Minimum Viable Organization (MVO) for LiNKtrend AIOS that is operational by March 15, 2026, with:
1. Paperclip live as orchestration control plane.
2. CEO OpenClaw live.
3. CTO OpenClaw live.
4. One operational development squad live.
5. Delegation flow active for AIOS and LiNKskills completion tasks.

## 3) Locked Decisions
1. Paperclip is mandatory and runs as a dedicated orchestration service.
2. Paperclip is not a bot runtime.
3. One internal AIOS polyglot monorepo will be created.
4. Paperclip is integrated in the monorepo via deployment/configuration, not full source vendoring.
5. Agent Zero workers run under OpenClaw managerial hierarchy.
6. Hosting split is hybrid:
   - VPS: Paperclip + CEO + CTO + core orchestration stack.
   - Mac mini: Agent Zero coding/QA workers and local-model-assisted execution.
7. Supabase architecture is one project with:
   - shared collective memory
   - private scratch memory per agent
8. LiNKskills MVO scope is coding-only core.

## 4) Scope
### In Scope (MVO)
1. New internal monorepo bootstrap.
2. VPS deployment for orchestration and manager agents.
3. Mac mini worker execution path.
4. Shared/private memory pipeline on managed Supabase.
5. LiNKskills Core for coding workflows.
6. End-to-end delegation and reporting loop (CEO -> CTO -> Squad).

### Out of Scope (Post-MVO)
1. Full department expansion across all AIOS roles.
2. Full LiNKskills library completion.
3. External client-facing LiNKbots packaging.
4. High-availability multi-node orchestration.

## 5) MVO Operating Topology
### Leadership and Management
1. Human Chairman
2. CEO (OpenClaw)
3. CTO (OpenClaw)
4. Squad Lead (OpenClaw)

### Worker Layer
1. Developer Worker (Agent Zero)
2. QA Worker (Agent Zero)

### Control Plane and Data Plane
1. Paperclip (orchestration and governance)
2. Supabase (shared + scratch memory + vector retrieval)
3. LiNKskills Core (coding tools and workflow wrappers)

## 6) Monorepo Strategy
Create one new internal monorepo (example: `linktrend-aios`) with this structure:

1. `infra/`  
VPS bootstrap, docker compose, reverse proxy, TLS, secrets injection.
2. `orchestration/`  
Paperclip service configs, org bootstrap, heartbeats, budget rules.
3. `bots/openclaw/`  
CEO/CTO/squad-lead profiles, prompts, routing contracts.
4. `bots/agent-zero/`  
Developer/QA worker profiles, runtime wrappers, execution policies.
5. `skills-core/`  
Coding LiNKskills Core modules and interfaces.
6. `memory/`  
Supabase schema definitions, policies, retrieval/write contracts.
7. `ops/`  
Runbooks, observability, incident response.
8. `docs/`  
ADR, architecture, acceptance tests, handover docs.

## 7) Hosting Strategy
### VPS Baseline
1. Linux VPS: `4 vCPU / 16GB RAM`
2. Runs:
   - Paperclip
   - CEO OpenClaw
   - CTO OpenClaw
   - LiNKskills Core services
   - reverse proxy and secure remote access

### Mac mini Baseline
1. Mac mini M2, 16GB RAM, 512GB SSD
2. Runs:
   - Agent Zero Developer worker
   - Agent Zero QA worker
   - optional local model runtime for low-cost coding tasks

### Supabase
1. Managed Cloud project
2. Single project for AIOS memory

## 8) Memory Strategy
### Shared Memory
Centralized long-term collective memory used by all AIOS agents.

### Scratch Memory
Private per-agent workspace memory for transient details.

### Policy
1. Agents read from shared memory at task start.
2. Agents read/write own scratch memory during task execution.
3. Task close includes summary write-back to shared memory.

## 9) LiNKskills Core (MVO)
Only coding-critical capabilities are required:
1. Repo operations (clone/pull/branch/status/commit metadata)
2. Code search/edit wrappers
3. Build/test/lint execution wrappers
4. QA verification and report generation
5. Memory bridge (shared + scratch operations)
6. Task bridge (status/comments/artifacts back to orchestration)

## 10) Delivery Plan (March 10-15, 2026)
### March 10
1. Monorepo initialization.
2. Environment model and secret convention finalized.
3. Infrastructure baseline skeleton committed.

### March 11
1. VPS provisioned and hardened.
2. Paperclip deployed and reachable.
3. CEO and CTO OpenClaw endpoints connected.

### March 12
1. Squad lead and worker routing enabled.
2. Mac mini workers connected to control flow.
3. Delegation loop validated on test tasks.

### March 13
1. Supabase shared/scratch schema deployed.
2. Retrieval and write-back contracts integrated.
3. Memory smoke tests passed.

### March 14
1. LiNKskills Core coding set integrated.
2. End-to-end coding task execution run.
3. QA artifact and status reporting validated.

### March 15
1. Full acceptance suite executed.
2. Budget guardrails enabled.
3. MVO go-live decision issued.

## 11) Acceptance Criteria for Go-Live
1. Paperclip control plane is stable and reachable.
2. CEO and CTO complete at least one successful operational cycle each.
3. One squad executes coding tasks with PLAN -> BUILD -> TEST -> QA -> REPORT.
4. Shared and scratch memory behaviors are verified.
5. Tasks for AIOS and LiNKskills completion are delegated and tracked.
6. Cost telemetry and budget limits are visible and active.

## 12) Risks and Mitigations
### Risk 1: Deadline compression
- Mitigation: strict MVO scope lock, no non-essential features.

### Risk 2: Integration fragility
- Mitigation: explicit delegation payload contracts and replayable tests.

### Risk 3: Cost spikes
- Mitigation: local-model-first for worker tasks and per-agent budget caps.

### Risk 4: Memory quality drift
- Mitigation: structured write templates and manager-curated memory promotion.

### Risk 5: Single-node orchestration bottleneck
- Mitigation: offload heavy execution to Mac mini; keep VPS orchestration-centric.

## 13) Post-MVO Immediate Next Steps
1. Expand squad into full FE/BE/FS worker specialization.
2. Expand LiNKskills beyond coding core.
3. Increase AIOS department coverage following org v2.0.
4. Add stronger HA/backup strategy for control plane.

