# Product Requirements Document (PRD)
# LiNKbrain — Memory, Audit, and Institutional Intelligence Layer

Document date: 2026-03-27  
Status: Draft (Phase 2)  
Owner: LiNKtrend Venture Factory  

## 1. Product Summary

LiNKbrain is the Venture Factory’s memory and audit layer. It is the system of record for mission state, governance decisions, execution evidence, institutional lessons, and the structured context required to make the organization coherent over time. In an AI-native organization, memory is not a convenience. It is the substrate that makes autonomy safe and compounding. Without a memory plane, the workforce becomes stateless, repetition becomes inevitable, and governance becomes impossible because decisions cannot be reconstructed reliably.

LiNKbrain is implemented as a hybrid memory system. It must support deterministic storage for structured operational truth (missions, tasks, policies, approvals, audit runs) and semantic retrieval for institutional knowledge and prior context (lessons, patterns, relevant historical artifacts). It must also support retention and compliance requirements that turn “logs” into investor-grade evidence.

LiNKbrain is not the control plane (LiNKaios), not the logic authority (LiNKskills), not the automation engine (LiNKautowork), not the workforce system (LiNKbots), and not an implementation platform (LiNKapps/LiNKsites). LiNKbrain is the memory substrate those systems rely upon.

## 2. Context and Problem Statement

Stateless execution is the default failure mode of agentic systems. When a system cannot reliably persist what happened and why, it cannot learn and it cannot be governed. The organization becomes dependent on human recall or on scattered local files. Even when “logs” exist, they are often not structured as a system of record. They may not be tenant-scoped. They may not be attributable to identity. They may not be reconstructable as an audit trail.

The Venture Factory requires memory to be: authoritative, structured, tenant-isolated, and auditable. It must allow reconstruction of mission progress, task outcomes, and protected decisions. It must allow retrieval of lessons and patterns to improve future execution. It must support a controlled promotion model so that low-quality noise does not become institutional truth. It must support retention windows and compliance posture suitable for both internal governance and external fundraising and commercialization.

LiNKbrain exists to provide this foundation.

## 3. Objectives and Success Criteria

LiNKbrain must provide an authoritative, tenant-scoped system of record for the Venture Factory. It must support strict access controls so agents cannot bypass governance by directly manipulating tables. It must support both structured and semantic retrieval. It must integrate with the control plane so that mission/task transitions and approvals persist as authoritative records. It must integrate with the logic and automation planes so runs and receipts can be audited and billed. It must support a hot/cold storage lifecycle so large artifacts can be archived without losing traceability.

LiNKbrain is successful when: a mission can be reconstructed end-to-end; every protected decision has an authoritative record; execution runs can be traced to identity and lineage; lessons can be retrieved and reused; and retention policies are enforced without destroying audit integrity.

## 4. Users and Actors

LiNKbrain is consumed by all other core systems. LiNKaios uses it as the authoritative record of missions, tasks, approvals, and audit events. LiNKskills writes run and receipt metadata and ledger truth into it. LiNKautowork writes workflow execution telemetry into it. LiNKbots retrieve context and persist outputs under governance. Human governance roles consume briefing outputs derived from LiNKbrain and make protected decisions that are persisted into it.

External consumers appear in later phases, when clients require tenant-scoped audit trails and when investor diligence requires evidence exports. LiNKbrain must be designed for those requirements from the start even if not all external surfaces are active in the MVP.

## 5. Scope and Boundaries

LiNKbrain is responsible for: structured storage of system-of-record entities, tenant registry and guardrails, audit run persistence, policy and approval records, lessons and institutional knowledge objects, semantic retrieval support, retention enforcement, and archive pointer management for hot/cold storage.

LiNKbrain is not responsible for: orchestration decisions (LiNKaios), skill definition and execution logic (LiNKskills), workflow execution (LiNKautowork), workforce role definitions (LiNKbots), or producing venture artifacts (LiNKapps/LiNKsites). LiNKbrain must also not become an uncontrolled dumping ground; promotion into long-term memory must be governed.

## 6. Core Concepts and Objects

### 6.1 Tenant

Tenancy is the fundamental boundary. Every system-of-record entity must be tenant-scoped. Tenant context must be required for reads and writes. Tenant isolation must be enforced by database policy, not by caller convention.

### 6.2 Mission, Task, and Approval Records

Missions and tasks are the backbone of execution traceability. Approvals are the backbone of governance traceability. LiNKbrain must store these records in structured form so that the organization’s state can be reconstructed reliably.

### 6.3 Audit Run

An audit run is the canonical record of an execution transaction. It must include lineage identifiers (mission, run, task, DPR), status, timing, and structured details sufficient to reconstruct and diagnose behavior.

### 6.4 Lesson and Institutional Knowledge

Lessons are promoted knowledge objects derived from execution. They are not raw logs. They must be promoted under policy so that the memory plane compounds quality rather than accumulating noise.

### 6.5 Semantic Retrieval

LiNKbrain must support semantic retrieval as a first-class capability. Semantic retrieval is used to find relevant prior context, lessons, and artifacts based on meaning rather than exact keys.

### 6.6 Hot/Cold Storage Pointers

Large artifacts cannot remain in hot storage indefinitely. LiNKbrain must store pointers and checksums for archived artifacts so the organization can retrieve or prove existence without keeping everything in the hot path.

## 7. Functional Requirements

### 7.1 Schema and Entity Model

LiNKbrain must define explicit schemas that separate tenant registry and shared guardrails from long-term institutional memory and scratch working memory. It must define the required tables for missions, policies, proposals, lessons, and audit runs, plus a scratch-memory layer for transient entries.

### 7.2 Access Control and RPC-First Safety

Agents must be forbidden from direct table access in the production contract. Sensitive operations must be performed through controlled functions so that the system can enforce tenant context, validate caller identity, and preserve audit integrity. This is a security requirement and a governance requirement.

### 7.3 Memory Promotion and Governance

The system must provide a promotion model that determines what transient entries become durable lessons. Promotion must be auditable and must support protected approvals when required. The system must support a “requires review” posture for auto-promotions until delegation policy changes.

### 7.4 Retention and Purge

LiNKbrain must enforce retention windows that distinguish between success metadata, failure diagnostics, disclosure/receipt metadata, and financial ledger truth. Retention must be enforced through automated workers with auditable confirmations.

### 7.5 Semantic Indexing and Embeddings

LiNKbrain must support vector indexing for semantic retrieval. Embeddings must have defined dimensionality and model selection standards. Embeddings must be computed in a way that preserves tenant isolation and does not leak sensitive content.

### 7.6 Archive Lifecycle (Hot/Cold Storage)

The system must support a hot/cold lifecycle where active artifacts live in hot storage and older artifacts migrate to cold storage under defined triggers. Archive operations must verify checksums and must persist pointers and metadata into LiNKbrain. Restore must be governed as a protected action when required.

## 8. Non-Functional Requirements

LiNKbrain must be reliable and performant under concurrency. It must support high read/write throughput for audit and workflow telemetry while preserving integrity. It must support backups and disaster recovery. It must support strict tenant isolation and prevent cross-tenant leakage. It must support privacy and compliance requirements suitable for commercialization and for investor diligence.

## 9. Roadmap by Phase

### 9.1 MVP (MVO)

The MVP delivers the canonical structured memory plane for a single internal tenant. It includes required schemas and tables, strict tenant context enforcement, audit run persistence, promotion scaffolding, vector search capability, retention policies, and archive pointer scaffolding. It integrates with LiNKaios task and approval flows, LiNKskills run and receipt flows, and LiNKautowork workflow telemetry flows.

### 9.2 PMF

The PMF phase hardens memory promotion and governance automation, expands semantic retrieval and indexing discipline, improves observability of memory health, and strengthens retention enforcement and archive workflows. It begins supporting multiple ventures under the internal tenant context and prepares multi-tenant commercialization posture.

### 9.3 Full-Scale

Full-scale LiNKbrain supports robust multi-tenant operation for internal ventures and external clients, mature compliance and retention programs, enterprise-grade evidence export, and a stable institutional knowledge compounding loop that materially improves Venture Factory throughput over time.

## 10. Appendix: Phase 1 Truth Sources

This PRD is written as a from-zero product definition, but it must align with Phase 1 truth sources, including:

- Venture Factory process authority: `/Users/linktrend/Projects/LiNKsmartfile/01-Studio-HQ/260326 - LiNKtrend Venture Factory Building Process.md`
- AIOS canonical memory contract: `/Users/linktrend/Projects/LiNKaios/docs/AIOS_MASTER_SPEC.md`
- LiNKbrain schema implementation surface: `/Users/linktrend/Projects/LiNKaios/packages/linkbrain`
