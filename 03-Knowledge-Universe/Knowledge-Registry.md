---
title: Knowledge Registry
type: knowledge
tags: [#knowledge, #registry, #memory, #vault, #helixdb]
created: 2026-06-20
updated: 2026-06-20
version: "6.0.0"
---

# 🌌 HGI V6 Knowledge Registry

This registry maps out the dual memory backend and the Obsidian-based knowledge network of the **RE-EVOLVE ON HGI V6** platform.

---

## 1. Relational & Vector Storage Layer (PostgreSQL)
The primary storage system for operational data and semantic embedding vectors.
- **Postgres Database:** `hgi_v6` (Target production schema)
- **Vector Storage:** Enabled via the `pgvector` extension.
- **Key Tables:**
  - `users`: Account identities, email/password credentials, and JWT decoded role metrics.
  - `ventures`: Active product developments, valuations, and roadmap nodes.
  - `agents`: Active agent state tracker, codenames, and capabilities.
  - `intelligence`: Extracted OSINT, research summaries, and strategic findings.
  - `memory_vectors`: Floating 1024-dimensional semantic arrays mapping agent memories.
  - `sessions`: Cache records containing Active Session IDs.
  - `audit_logs`: Detailed compliance change entries.

---

## 2. Graph-Vector Layer (HelixDB)
Multi-hop relationship mapping for associative cognitive retrieval.
- **System Integration:** [helix-backend.ts](file:///Users/nextunicorn/packages/memory/src/backends/helix-backend.ts)
- **Local Dev Endpoint:** `http://localhost:6969` (Docker runtime)
- **Capabilities:**
  - Graph node-link traversal (linking agents, ventures, and research findings).
  - High-performance vector similarity search in Rust.
  - Real-time memory relationship mapping.

---

## 3. Obsidian Knowledge Vault Layer
Human-readable documentation and decision records stored as structured markdown notes in the `HGI-Vault` workspace.

### Vault Subdirectory Structure

| Folder | Purpose | Major Files | Owner Agent |
| :--- | :--- | :--- | :--- |
| **00-Foundation** | Long-term vision and architecture | HGI-Vision.md, HGI-V6-Architecture.md, Architecture-Registry.md | LUMEN |
| **01-HQ-V6** | Design system documentation | V6-Tokens.md, V6-Dashboard-Build.md | NOVA / FORGE |
| **02-Agents** | Agent profiles and assignments | INDEX.md, Agent-Registry.md, individual agent folders | LUMEN |
| **03-Knowledge-Universe** | Research, memory, and sync metrics | INDEX.md, Knowledge-Registry.md | CENSA |
| **04-Venture-Civilization** | Venture studio assets | INDEX.md, product plans | VANTIS |
| **05-Creative-Intelligence**| Programmatic audio/video details | INDEX.md, Remotion configs | NOVA |
| **06-Operations** | Deployment blueprints and registries | System-Registry.md, Current-Deployment.md, Security-Audits | SAROS / AEGIS |
| **Daily Notes** | Dynamic logs for chronological entries | 2026-06-20.md, Daily updates | All Agents |
| **Templates** | Unified note layouts | Agent-Memory.md, meeting templates | LUMEN |
| **99-Archive** | Deprecated designs and specs | Older v5 checklists | LUMEN |

---

## 4. Source Lineage & System Synchronization Logs
Operational audit logs tracking the alignment of knowledge files.
- **Sync Log:** [hgi-sync.log](file:///Users/nextunicorn/hgi-sync.log) (captures synchronization events between local vaults and cloud endpoints).
- **Agent Self-Evolution Log:** [hermes-self-evolve.log](file:///Users/nextunicorn/hermes-self-evolve.log) (tracks decisions parsed and compiled back into markdown files by the active controller).

---
*[[../VAULT-INDEX|← Home]]*
*[[../00-Foundation/Architecture/Architecture-Registry|Architecture Registry →]]*
