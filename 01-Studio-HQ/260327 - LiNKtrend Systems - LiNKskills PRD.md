# Product Requirements Document (PRD)
# LiNKskills — Governed Skill and Logic Engine

Document date: 2026-03-27  
Status: Draft (Phase 2)  
Owner: LiNKtrend Venture Factory  

## 1. Product Summary

LiNKskills is the logic authority of the LiNKtrend Venture Factory. It defines, governs, versions, and serves the executable methods that power the organization’s workforce, automation, and products. In the Venture Factory architecture, LiNKaios decides what should happen next, LiNKbots perform work, LiNKautowork executes deterministic workflows, and LiNKbrain stores the record of truth. None of those systems, however, should be the place where reusable procedural logic lives. LiNKskills is the system that isolates logic from execution so that the organization’s behavior can be standardized, improved, audited, and monetized without turning every bot into its own inconsistent prompt universe.

LiNKskills begins as an internal operating layer: a governed catalog of skills and tools used by the digital workforce. It evolves into a multi-tenant product: a central “Logic Engine” that serves skills and packages via controlled contracts to internal systems and, later, to external clients. The product must satisfy a tension that most skill libraries do not solve: it must be usable at scale while remaining governable and protectable. The system must allow execution without distributing full internal logic everywhere, and it must preserve central control over quality, policy, entitlement, versioning, identity requirements, retention, and billing.

## 2. Context and Problem Statement

In agent-based systems, logic naturally fragments. Each agent accumulates its own prompts, procedures, and tool usage patterns, and the system slowly becomes a collection of idiosyncratic behaviors rather than a coherent organization. Even when the same “task” is executed repeatedly, outputs drift because the underlying method is not encoded as a stable artifact. As the number of ventures and bots increases, this drift becomes a structural failure: quality degrades, governance becomes impossible, and the organization becomes dependent on founder memory to compensate for inconsistency.

The Venture Factory cannot industrialize venture creation unless logic is centralized. Centralization is not a style preference; it is an economic and governance requirement. It enables reuse, reduces marginal cost, and makes improvements compounding rather than local. It also enables controlled commercialization, because the organization’s logic is itself a monetizable asset only if it can be packaged, metered, and delivered safely.

LiNKskills exists to eliminate logic drift and to make execution repeatable. It provides a canonical definition of what a skill is, how it is authored, how it is validated, how it is executed, how it is audited, and how it evolves over time.

## 3. Objectives and Success Criteria

LiNKskills must provide a single source of truth for reusable logic across the Venture Factory. It must allow different execution substrates (OpenClaw, Agent Zero, workflow engines, application backends) to execute the same governed skill contract and produce consistent, auditable outputs. It must separate authoring from runtime delivery so that the system can remain maintainable without sacrificing operational usability. It must support strict identity and idempotency contracts so that managed execution is safe and reconstructable. It must support an explicit policy model that allows internal execution now and commercialization later without redesigning the entire system.

LiNKskills is successful when the organization can point to a capability and say: this is the method, this is the version, this is the policy, this is the audit record, this is the cost, and this is the outcome. It is also successful when new skills can be created and promoted without destabilizing the system, and when governance can block or roll back unsafe logic quickly.

## 4. Users and Actors

Internally, the primary consumers of LiNKskills are LiNKaios (control-plane invocations), LiNKautowork (workflow steps that require governed logic), and LiNKbots (workforce execution that depends on standardized methods). Internally, the primary operators of LiNKskills are the platform and governance roles responsible for skill authoring, validation, promotion, and lifecycle control.

Externally, later phases introduce client consumers: external ventures, partner organizations, and customers who purchase access to specific skills or packages. In those scenarios, the system must enforce tenant isolation, entitlement, and controlled exposure modes without assuming that the client environment is trusted.

## 5. Product Scope and Boundaries

LiNKskills is responsible for: defining the skill artifact standard, providing a governed authoring and validation workflow, maintaining an authoritative catalog of skills and packages, serving skills through controlled contracts, enforcing identity and idempotency on execution paths, issuing run identifiers and receipts, persisting audit and cost records into LiNKbrain, enforcing retention policies, and implementing kill-switch behavior for safety and runaway cost control.

LiNKskills is not responsible for: orchestrating missions and tasks (LiNKaios), executing deterministic workflows (LiNKautowork), serving as the persistent memory store (LiNKbrain), acting as the workforce substrate (LiNKbots), or building venture implementation artifacts (LiNKapps and LiNKsites). LiNKskills also must not become an ungoverned marketplace of arbitrary community logic; the system’s defining property is governed quality and policy enforcement.

## 6. Core Concepts and Objects

### 6.1 Skill

A skill is a governed logic artifact that encodes a method for executing a task class. It is not “a prompt.” It includes structure, constraints, input and output contracts, persistence rules, and explicit boundaries for what is allowed. Skills must be versioned and must carry lifecycle metadata so that execution can be pinned, certified, deprecated, and rolled back.

### 6.2 Package

A package is an ordered composition of skills that represents a larger reusable capability. Packages exist because real work is multi-step. Packages must be executable under controlled sequencing rules in the managed execution mode, with stable step ordering and explicit contracts between steps.

### 6.3 Managed Execution

Managed execution is the execution mode where the Logic Engine remains the authority for what runs and how. The caller does not receive the full internal logic by default. The system issues a run identifier, performs policy checks, and executes governed steps, producing receipts and auditable metadata. This is the MVP posture because it enables central governance and IP protection while still allowing the workforce and automations to consume standardized capabilities.

### 6.4 Identity and Tenancy

Execution must be tenant-scoped. Every run must include tenant identity and a principal identity. AIOS-origin requests must also include mission and task lineage and a workforce identity identifier (DPR). These identity fields are not optional metadata. They are the basis for auditability, permission enforcement, and cost allocation.

### 6.5 Idempotency

Write operations must be idempotent under a defined window. The system must guarantee that repeated calls with the same key and same normalized payload produce the same result and do not double-bill or double-execute. If the same key is reused with a different payload, the system must reject with a conflict response.

## 7. Functional Requirements

### 7.1 Catalog and Discovery

LiNKskills must expose a governed catalog of skills and packages. Catalog entries must include identity, versioning, lifecycle state, policy class, and metadata required for safe consumption. Catalog discovery must support internal consumption first, with external discovery enabled only when policy permits.

### 7.2 Run Creation and Receipts

LiNKskills must support run creation as a first-class object. A run is the unit of execution and billing. The system must generate run identifiers, enforce identity and idempotency requirements at ingress, and persist run metadata. After execution, the system must emit receipts that capture what executed, what it cost, what policy gates were applied, and what outcome was produced.

### 7.3 Policy and Class Model

LiNKskills must support a class model that separates launch-active internal capabilities from deferred commercial capabilities and from hidden future scopes. The system must be able to enforce class boundaries in execution mode and in catalog visibility. The class model must be strong enough to allow scaffolding without accidental activation.

### 7.4 Secrets and Safe Mode

LiNKskills must resolve secrets through a managed secret source in production, and it must fail closed on secret retrieval failure for execution paths. The system must enter a controlled safe mode when required secrets cannot be resolved, preserving health and visibility endpoints while refusing execution writes.

### 7.5 Retention and Compliance

LiNKskills must implement explicit retention behavior. Successful runs must store metadata only unless policy requires deeper retention. Failures may retain redacted diagnostics for a bounded window. Disclosure and receipt metadata must have defined retention. Financial ledger records must meet multi-year retention requirements.

### 7.6 Kill Switch

LiNKskills must implement a kill-switch hierarchy that can halt new execution under defined runaway cost or security anomaly conditions, allow in-flight runs to complete by default, and support emergency cancellation when necessary. Kill-switch events must be auditable and reversible through governed restore actions.

## 8. Architecture (Logical and Operational)

LiNKskills is architected as two coordinated planes.

The authoring and governance plane is the skill repository that defines standards, structures, validation, and the canonical catalog. This plane is where skills are created, reviewed, certified, and promoted through lifecycle states.

The runtime control plane is the Logic Engine service that executes skills in managed mode under enforced identity and policy contracts. The runtime plane exposes a controlled API surface for catalog reads, run creation, execution, receipts, and ops telemetry.

The system’s memory and financial source of truth is LiNKbrain. LiNKskills must therefore integrate with the memory plane for audit persistence and ledger writes, rather than creating a separate competing truth for execution history.

## 9. Roadmap by Phase

### 9.1 MVP (MVO)

The MVP delivers internal-only managed execution for the canonical internal tenant. It provides a REST-first API surface, strict identity requirements for AIOS-origin calls, idempotency on write paths, run creation and receipt issuance, GSM-backed secret resolution, safe-mode behavior, retention enforcement, and kill-switch behavior. It integrates as a first-class dependency of LiNKaios and LiNKautowork.

### 9.2 PMF

The PMF phase hardens the product for repeated internal throughput, expands governance automation, and begins introducing commercialization scaffolding with strict non-activation guarantees. It improves catalog usability, adds stronger entitlement enforcement, improves observability, and strengthens audit reconstruction and cost attribution.

### 9.3 Full-Scale

Full-scale LiNKskills becomes a multi-tenant commercial Logic Engine with controlled exposure modes, mature entitlement and billing surfaces, MCP transport support where policy allows, and a stable packaging model that allows external customers to consume governed logic without receiving full internal source by default. It supports robust rollback and certification, enterprise-grade auditing, and clear productized offerings.

## 10. Appendix: Phase 1 Truth Sources

This PRD is written as a from-zero product definition, but it must align with the Phase 1 source-of-truth materials and the reference repos, including:

- Venture Factory process authority: `/Users/linktrend/Projects/LiNKsmartfile/01-Studio-HQ/260326 - LiNKtrend Venture Factory Building Process.md`
- LiNKskills reference implementation: `/Users/linktrend/Projects/LiNKskills` (including `260319 LiNKskills PRD.md` and `services/logic-engine`)
- AIOS integration contract context: `/Users/linktrend/Projects/LiNKaios/docs/AIOS_MASTER_SPEC.md`
