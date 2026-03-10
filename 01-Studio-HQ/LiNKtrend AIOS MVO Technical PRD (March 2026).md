# LiNKtrend AIOS MVO Technical PRD (March 2026)

## 1) Product Metadata
- Product: `LiNKtrend Autonomous AIOS`
- Release: `MVO v1`
- PRD Version: `1.0`
- Date: `March 10, 2026`
- Target Go-Live Date: `March 15, 2026`
- Owner: `LiNKtrend Chairman / Executive Layer`

## 2) Problem Statement
LiNKtrend requires an operational AI-first organizational core that can execute technical delivery autonomously with governance, delegation, memory continuity, and cost control. Existing architecture direction is defined, but MVO needs to be operational quickly to accelerate completion of full AIOS and LiNKskills.

## 3) Product Objective
Deliver a production-usable MVO by March 15, 2026 that includes:
1. Paperclip orchestration live.
2. CEO OpenClaw and CTO OpenClaw live.
3. One operational development squad.
4. Delegation and execution pipeline for AIOS and LiNKskills tasks.
5. Shared collective memory plus private scratch memory.

## 4) Goals
1. Operational governance and command chain through Paperclip.
2. Reliable manager-to-worker delegation (OpenClaw -> Agent Zero).
3. Codified coding workflow with QA gates.
4. Persistent organizational memory with controlled sharing.
5. Cost-aware operations within initial budget target.

## 5) Non-Goals (MVO Phase)
1. Full department expansion across all org v2.0 roles.
2. Full LiNKskills library completion.
3. Multi-node high availability architecture.
4. External client bot productization.

## 6) Users and Personas
1. Human Chairman
2. CEO OpenClaw (strategic management)
3. CTO OpenClaw (technical management)
4. Squad Lead OpenClaw (flow management)
5. Agent Zero Developer worker
6. Agent Zero QA worker

## 7) System Architecture
### 7.1 Control Plane
1. Paperclip service deployed on VPS.
2. Org chart, heartbeats, budget controls, and governance managed in Paperclip.

### 7.2 Management Layer
1. CEO and CTO implemented as OpenClaw instances.
2. OpenClaw handles reasoning, coordination, and delegation.

### 7.3 Execution Layer
1. Agent Zero workers execute terminal-based build/test/QA tasks.
2. Workers are subordinate to OpenClaw management.

### 7.4 Memory Layer
1. Managed Supabase project.
2. Shared memory for collective knowledge.
3. Private scratch memory for per-agent transient context.

### 7.5 Skills Layer
1. LiNKskills Core coding package.
2. Centralized wrappers for repo, code, test, QA, memory, and task updates.

## 8) Infrastructure and Deployment Requirements
### 8.1 VPS Requirements
1. Linux VPS minimum `4 vCPU / 16GB RAM`.
2. Must host:
   - Paperclip
   - CEO OpenClaw
   - CTO OpenClaw
   - LiNKskills Core services
   - proxy/security layer

### 8.2 Mac mini Requirements
1. Mac mini M2 16GB used for:
   - Agent Zero Developer worker
   - Agent Zero QA worker
   - local-model-assisted tasks where cost-efficient

### 8.3 Networking and Security
1. Secure connectivity between VPS and Mac mini.
2. TLS for exposed services.
3. Secrets via environment/vault, never hardcoded.

## 9) Repository Requirements
One internal polyglot monorepo must be created with at least:
1. `infra/`
2. `orchestration/`
3. `bots/openclaw/`
4. `bots/agent-zero/`
5. `skills-core/`
6. `memory/`
7. `ops/`
8. `docs/`

Paperclip is integrated as a service dependency/configuration target in this monorepo, not copied as full upstream source unless core modifications become mandatory.

## 10) Functional Requirements
`FR-001` Company bootstrap must instantiate org hierarchy and role links.  
`FR-002` CEO/CTO must run heartbeat cycles with task continuity.  
`FR-003` CTO/Squad Lead must assign coding tasks to workers and receive status/artifacts.  
`FR-004` Worker flow must enforce PLAN -> BUILD -> TEST -> QA -> REPORT.  
`FR-005` LiNKskills Core must be callable by worker execution routines.  
`FR-006` Shared memory writes must occur at task completion.  
`FR-007` Scratch memory must be private per agent.  
`FR-008` Task start must include memory retrieval hooks.  
`FR-009` Cost telemetry and budget limits must be active in control plane.  
`FR-010` Audit trail must include run_id, task_id, agent_id, status transitions, and key actions.

## 11) Non-Functional Requirements
`NFR-001` MVO must be deployable by March 15, 2026.  
`NFR-002` System should operate near initial target budget of `$500/month`.  
`NFR-003` Control-plane failures must not corrupt memory/task state.  
`NFR-004` All credentials must be centrally managed and rotatable.  
`NFR-005` Logs and health checks must support operational debugging.

## 12) Data Requirements
### 12.1 Shared Memory Table
Required fields:
1. `id`
2. `agent_id`
3. `role`
4. `task_id`
5. `project_id` (default `AIOS`)
6. `content_md`
7. `content_json`
8. `embedding`
9. `created_at`

### 12.2 Scratch Memory Table
Same shape as shared memory but scoped read/write to owner agent.

### 12.3 Policy Model
1. All agents can read shared memory.
2. All agents can write shared memory.
3. Agent can only read/write own scratch rows.
4. Promotion from scratch to shared is explicit.

## 13) LiNKskills Core Requirements (Coding)
Minimum modules:
1. `repo-ops`
2. `code-search-edit`
3. `build-test-runner`
4. `qa-verifier`
5. `memory-bridge`
6. `task-bridge`

## 14) Acceptance Criteria (Go-Live)
1. Paperclip reachable and stable.
2. CEO and CTO each complete one successful operational cycle.
3. Squad executes at least one coding task end-to-end with QA artifact.
4. Shared and private memory behaviors are validated.
5. AIOS and LiNKskills continuation tasks are delegated through chain of command.
6. Budget telemetry and guardrails are active.

## 15) Timeline
1. March 10: Monorepo and infra skeleton.
2. March 11: VPS + Paperclip + CEO/CTO integration.
3. March 12: Squad routing + Mac mini worker connection.
4. March 13: Supabase memory schema and contracts.
5. March 14: LiNKskills Core integration and end-to-end test.
6. March 15: Acceptance run and MVO go-live decision.

## 16) Dependencies
1. VPS provision and access.
2. Managed Supabase credentials and project ready.
3. OpenRouter/model credentials.
4. Mac mini availability.
5. Paperclip/OpenClaw/Agent Zero pinned baseline versions.

## 17) Risks and Mitigations
1. Scope overrun risk  
Mitigation: strict MVO feature lock.
2. Integration risk across agent layers  
Mitigation: fixed delegation contract and replayable tests.
3. Cost volatility risk  
Mitigation: local-model-first routing and budget caps.
4. Memory contamination risk  
Mitigation: explicit shared/scratch policies and structured write format.

## 18) Open Questions (Post-MVO)
1. Final full-squad role count and specialization model.
2. Long-term monorepo toolchain standard.
3. HA model and disaster recovery strategy.
4. External LiNKbot packaging standards.

---

## Appendix A: Machine-Ready Delivery Backlog (Epics -> Stories -> Acceptance Tests)

### Epic E1: Control Plane Foundation
#### Story E1-S1
- Build Paperclip deployment stack on VPS.
- Acceptance tests:
  1. API health endpoint responds.
  2. UI accessible.
  3. Persistent state survives restart.

#### Story E1-S2
- Bootstrap company hierarchy in Paperclip.
- Acceptance tests:
  1. CEO, CTO, Squad Lead entities exist.
  2. Reporting lines match architecture.

### Epic E2: Manager Agent Layer
#### Story E2-S1
- Integrate CEO OpenClaw runtime with Paperclip control loop.
- Acceptance tests:
  1. CEO receives and acknowledges task context.
  2. CEO emits status updates to control plane.

#### Story E2-S2
- Integrate CTO OpenClaw runtime with delegation capability.
- Acceptance tests:
  1. CTO receives strategic tasks.
  2. CTO delegates to squad workers.

### Epic E3: Worker Execution Layer
#### Story E3-S1
- Connect Agent Zero Developer worker on Mac mini.
- Acceptance tests:
  1. Worker receives task payload.
  2. Worker executes repo/code/test actions.

#### Story E3-S2
- Connect Agent Zero QA worker on Mac mini.
- Acceptance tests:
  1. QA worker runs validation pipeline.
  2. QA report is returned to manager layer.

### Epic E4: Memory Fabric
#### Story E4-S1
- Implement shared memory table and write/read adapters.
- Acceptance tests:
  1. All agents can retrieve shared entries.
  2. New task learnings can be stored and queried.

#### Story E4-S2
- Implement per-agent scratch memory and policy enforcement.
- Acceptance tests:
  1. Agent can read/write own scratch records.
  2. Cross-agent scratch access is blocked.

### Epic E5: LiNKskills Core
#### Story E5-S1
- Implement coding skill wrappers (repo, code, build, test).
- Acceptance tests:
  1. Skills execute deterministically.
  2. Return schema is stable.

#### Story E5-S2
- Integrate memory and task bridges into LiNKskills Core.
- Acceptance tests:
  1. Skills can write memory summaries.
  2. Skills can post task progress back to control plane.

### Epic E6: End-to-End MVO Validation
#### Story E6-S1
- Execute AIOS continuation task via full hierarchy.
- Acceptance tests:
  1. Task passes through CEO -> CTO -> Squad.
  2. Completion artifact and status are recorded.

#### Story E6-S2
- Execute LiNKskills continuation task via full hierarchy.
- Acceptance tests:
  1. Task passes through CEO -> CTO -> Squad.
  2. Completion artifact and status are recorded.

---

## Appendix B: Strict Execution Checklist for AI Coding Agent

### Phase 0: Preconditions
1. Confirm VPS access.
2. Confirm Supabase project and credentials.
3. Confirm model credentials.
4. Confirm Mac mini online and reachable.
5. Confirm no blocking dependency unresolved.

### Phase 1: Repo and Infra Bootstrap
1. Create monorepo structure.
2. Add infra deployment templates.
3. Add service environment templates.
4. Add baseline observability and health checks.
5. Validate local boot sequence.

### Phase 2: Paperclip Control Plane
1. Deploy Paperclip service.
2. Validate API/UI health.
3. Configure company and org bootstrap.
4. Configure heartbeat and budget settings.
5. Validate persistence across restart.

### Phase 3: OpenClaw Manager Layer
1. Configure CEO profile and runtime connection.
2. Configure CTO profile and runtime connection.
3. Validate CEO/CTO heartbeat cycles.
4. Validate task acknowledgment and status reporting.

### Phase 4: Agent Zero Worker Layer
1. Configure Developer worker runtime.
2. Configure QA worker runtime.
3. Validate manager-to-worker delegation payload.
4. Validate worker-to-manager completion payload.

### Phase 5: Supabase Memory Fabric
1. Create shared memory schema.
2. Create scratch memory schema.
3. Apply access policies.
4. Validate shared retrieval.
5. Validate scratch isolation.

### Phase 6: LiNKskills Core
1. Implement repo-ops wrapper.
2. Implement code-search-edit wrapper.
3. Implement build-test-runner wrapper.
4. Implement qa-verifier wrapper.
5. Implement memory-bridge wrapper.
6. Implement task-bridge wrapper.
7. Validate all wrapper contracts.

### Phase 7: End-to-End Validation
1. Execute one AIOS completion task.
2. Execute one LiNKskills completion task.
3. Verify PLAN -> BUILD -> TEST -> QA -> REPORT chain.
4. Verify memory writes and retrievals.
5. Verify cost telemetry and budget controls.
6. Produce final go-live report.

### Phase 8: Go-Live Decision Gate
1. Check all acceptance criteria.
2. Log unresolved blockers.
3. Decide `GO` or `NO-GO`.
4. If `GO`, freeze baseline and start post-MVO roadmap.

