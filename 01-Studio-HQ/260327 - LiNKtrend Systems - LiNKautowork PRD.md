# Product Requirements Document (PRD)
# LiNKautowork — Governed Automation Execution Engine

Document date: 2026-03-27  
Status: Draft (Phase 2)  
Owner: LiNKtrend Venture Factory  

## 1. Product Summary

LiNKautowork is the Venture Factory’s automation execution engine. It is the system that runs deterministic, repeatable workflows as governed process assets. Where LiNKbots are the workforce and LiNKskills is the logic authority, LiNKautowork is the process execution layer that turns logic and labor into stable operational pipelines. It exists to ensure that work which should be executed as a deterministic state machine is not executed as open-ended agent reasoning. It also exists to make workflows first-class organizational assets: versioned, validated, auditable, promotable, and eventually monetizable.

LiNKautowork is implemented on top of an automation substrate (n8n in the MVP posture), but the product is not “n8n.” The product is the governance overlay and the operational contract that makes automation reliable inside an AI-native organization. The system includes canonical templates, a lifecycle and promotion state machine, a policy gateway that enforces signed ingress and lineage validation, a canonical audit write path into LiNKbrain, and event interoperability into the Venture Factory event plane.

## 2. Context and Problem Statement

Automation tools are easy to adopt and hard to standardize. In ungoverned automation environments, workflows proliferate as one-off configurations. Over time, workflows drift in structure, error handling, secrets management, and integration contracts. They become difficult to audit and expensive to maintain. In the Venture Factory model, this failure mode is fatal because automation is not a convenience; it is a primary lever for reducing marginal cost and for making the organization executable.

The Venture Factory also requires a strict distinction between deterministic execution and adaptive reasoning. Adaptive reasoning belongs in LiNKbots and LiNKskills where judgment and interpretation are needed. Deterministic execution belongs in LiNKautowork so that routine processes can run on schedules, respond to events, and produce consistent outputs without creating token waste or uncontrolled variability.

LiNKautowork exists to solve three problems simultaneously: workflow determinism, workflow governance, and workflow interoperability. It must ensure that workflows run predictably; that changes to workflows are controlled, promoted, and evidenced; and that the rest of the system can rely on automation outputs as auditable system transactions rather than as fragile scripts.

## 3. Objectives and Success Criteria

LiNKautowork must provide a canonical automation template library and a governed promotion lifecycle. It must provide a security and policy gateway so that workflow invocation is attributable, tenant-scoped, and resistant to replay and unauthorized access. It must write canonical audit telemetry into the memory plane and publish events into the event plane so that automation execution is observable and reconstructable. It must support the Venture Factory’s daily ritual windows by producing scheduled outputs reliably even under degraded upstream conditions, explicitly flagging partial or low-confidence outputs instead of silently failing.

LiNKautowork is successful when the organization can treat workflows as production assets. A successful workflow has a known template source, a known version, known promotion evidence, known audit records for each run, and known failure handling and escalation paths. At scale, success means the organization can expand automation coverage without allowing the automation layer to become a chaotic mirror of the worst failure modes of human ops.

## 4. Users and Actors

Internally, the primary consumers of LiNKautowork are LiNKaios (which triggers workflows and consumes their outputs), LiNKbots (which may be invoked within workflows for bounded adaptive steps), and operational stakeholders who depend on ritual briefings and governance outputs. Internally, the primary operators are the roles responsible for workflow authoring, validation, QA, promotion, and operational reliability.

Externally, later phases include clients who consume workflow execution as a managed service or as packaged workflow templates. These external consumption modes require multi-tenant isolation, secrets handling, and policy controls that are present in the design from the start even if the MVP operates internal-only.

## 5. Scope and Boundaries

LiNKautowork is responsible for: canonical workflow templates, workflow lifecycle promotion and evidence, deterministic execution on schedules and event triggers, policy-gated ingress to prevent untrusted execution, canonical audit persistence for each run, event publishing for interoperability, kill-switch behavior for runaway incidents, and operational runbooks for deployment and maintenance.

LiNKautowork is not responsible for: deciding what work should exist or what work should happen next (LiNKaios), defining reusable logic methods (LiNKskills), storing the organization’s memory and audit truth (LiNKbrain), serving as the adaptive workforce (LiNKbots), or building venture implementation artifacts (LiNKapps and LiNKsites). LiNKautowork also must not become a place where arbitrary bespoke code is hidden; when workflow logic exceeds deterministic orchestration, it should be delegated into governed skills rather than embedded as unreviewable ad hoc nodes.

## 6. Core Concepts and Objects

### 6.1 Workflow Template

A workflow template is a version-controlled workflow definition that represents the canonical source of a workflow. Templates exist to prevent drift. A template is not “an export from prod” and it is not “whatever is in the UI right now.” It is the authoritative definition against which deployed instances are validated.

### 6.2 Lifecycle State Machine

Workflows must progress through a fixed lifecycle state machine so that promotion is evidence-driven. A workflow begins as draft, is tested in development, receives QA approval, receives ops approval, is deployed to production, and may later be deprecated and archived. Each transition must have explicit evidence requirements and defined approver roles.

### 6.3 Policy Gateway

Workflow execution must be invoked through a policy gateway rather than by direct access to workflow engine webhooks. The gateway validates signatures, blocks replay, validates tenant and lineage, resolves secrets just-in-time, writes canonical audit records, publishes events, and enforces kill-switch and lifecycle rules. This gateway is what converts “automation execution” into “governed system transaction.”

### 6.4 Audit Run Record

Every workflow execution must produce a canonical audit record that includes identity and lineage (tenant, run, task, DPR), status, latency and failure metadata, and structured details sufficient to reconstruct what happened. Audit records are written into LiNKbrain so that the memory plane remains the authoritative audit truth.

## 7. Functional Requirements

### 7.1 Template Authority

The system must define a single source of truth location for canonical templates. It must support validation of templates and must support import into the workflow engine runtime. The system must also support export of deployed workflow evidence for audit and parity verification.

### 7.2 Ingress Contract and Security Headers

Workflow invocation must require a strict ingress envelope containing tenant context and lineage identifiers, and it must require signed request headers sufficient to prevent unauthorized invocation and replay. The system must fail closed on invalid signatures, missing lineage, or tenant mismatch. These constraints must apply equally to internal callers and to future external callers because they are safety mechanisms rather than commercial features.

### 7.3 Event Publishing and Interoperability

Workflow execution must publish events into the Venture Factory event plane under canonical subjects so that other systems can react without bespoke integration. The system may support internal mirror subjects for LiNKautowork-specific consumers but must maintain interoperability as the default posture.

### 7.4 Ritual Outputs

The system must support scheduled ritual outputs that feed governance windows. These outputs must publish on schedule. If upstream data is degraded, outputs must still be produced with explicit confidence degradation rather than silently skipping publication.

### 7.5 Kill Switch

The system must support scoped kill switches (per tenant or workflow path) and a global kill switch (platform-wide webhook revocation) to respond to security incidents and runaway cost events. Kill-switch activation and restore must be auditable and subject to governance approvals for protected actions.

## 8. Non-Functional Requirements

LiNKautowork must be operable and reliable. It must provide health and readiness signals, explicit failure modes, runbooks, and backup/restore procedures. It must support safe secrets handling through managed secret infrastructure. It must support multi-tenant isolation as a design requirement, even if the MVP is internal-only.

## 9. Roadmap by Phase

### 9.1 MVP (MVO)

The MVP delivers internal-only automation execution under a canonical internal tenant. It provides canonical templates, a policy gateway, a governed lifecycle state machine, canonical audit persistence into Supabase (LiNKbrain), event publishing into NATS under canonical subjects, ritual workflows for daily briefing windows, and operational scripts for import/export, backup, and validation. It also delivers initial kill-switch behavior.

### 9.2 PMF

The PMF phase increases automation coverage, improves QA and promotion discipline, strengthens observability and alerting, and begins shaping the productization surface for external workflow packs and managed automation offerings. It expands the template library and strengthens the automation-to-billing linkage so that workflow execution can become a measurable and monetizable product line.

### 9.3 Full-Scale

Full-scale LiNKautowork supports multi-tenant external clients, self-service provisioning where policy allows, mature entitlement and metering, and a robust library of workflow packs by vertical or domain. It provides high-availability deployment patterns, mature incident response automation, and hardened interfaces that preserve the Venture Factory’s governance posture even under commercialization.

## 10. Appendix: Phase 1 Truth Sources

This PRD is written as a from-zero product definition, but it must align with the Phase 1 source-of-truth materials and reference repos, including:

- Venture Factory process authority: `/Users/linktrend/Projects/LiNKsmartfile/01-Studio-HQ/260326 - LiNKtrend Venture Factory Building Process.md`
- LiNKautowork reference implementation: `/Users/linktrend/Projects/LiNKautowork` (including templates, gateway, and lifecycle docs)
- AIOS integration contract context: `/Users/linktrend/Projects/LiNKaios/docs/AIOS_MASTER_SPEC.md`
