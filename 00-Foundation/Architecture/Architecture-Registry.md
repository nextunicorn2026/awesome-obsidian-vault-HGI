---
title: Architecture Registry
type: foundation
tags: [#foundation, #architecture, #registry, #design]
created: 2026-06-20
updated: 2026-06-20
version: "6.0.1"
---

# 🏛️ HGI V6 Architecture Registry

This document maps out the system architecture layers of the **RE-EVOLVE ON HGI V6** platform.

---

## 1. Cognitive Architecture Layer (CENSA)
The brain of the platform, orchestrating reasoning, intent mapping, and agent assignment.
- **Orchestration Core:** Powered by the `packages/orchestration` event fabric and `packages/censa-routing` context dispatcher.
- **Coordination Model:** Asynchronous Directed Acyclic Graphs (DAGs) resolved by **Sarathi Prime** (SAROS) and system status checks.
- **Model Routing:** Employs a dynamic cost-quality balancing strategy. Triage routes standard queries to `gpt-4o-mini` or `amazon.nova-micro-v1` and complex design/strategy tasks to `claude-sonnet-4-6`.

---

## 2. Interface Layer
Cross-platform surfaces for founders, developers, and agents.
- **Web App (Landing):** Next.js 14 marketing page. Utilizes `V2.ThemeProviderV2` with `adaptive-aurora` (a cinematic, dark-themed responsive design).
- **HQ (Command Nexus):** Next.js App Router workspace using `cosmic-dark` styling rules. Exposes 58 navigation endpoints under the `HGIShell` shell. Uses `withRBAC` for identity gatekeeping.
- **Desktop (Shell):** Electron-based standalone wrapper. Bypasses normal RBAC via `BETA_TEST_MODE`. Features automatic token injection into the Next.js HQ views via `executeJavaScript` on page load.
- **CLI (Developer Tool):** Interactive console (`packages/cli`) with Ora spinners, brand boot animations, and direct CLI command bridges for founder onboarding.

---

## 3. Execution & Tooling Layer (MCP)
External integrations and systems wired via the **Model Context Protocol (MCP)**.
- **Configured Servers:** Maintained in `.cursor/mcp.json`.
- **Active MCP Servers:**
  - `sequential-thinking` (cognitive reasoning flow)
  - `filesystem` (local workspace access)
  - `github` (repo code and issue management)
  - `playwright` (web browser session control)
  - `spider-web-intelligence` (Rust crawler exposing bulk scrapers)
  - `agent-reach` (platform-authenticated search endpoints for Reddit, YouTube, Exa)
  - `browser-use` (Python/Rust backend for autonomous web navigation)

---

## 4. Memory & Knowledge Layer
Hierarchical vector and graph persistence.
- **Relational Stores:** PostgreSQL `hgi_v6` production tables (users, ventures, agents, intelligence, sessions, audit logs).
- **Vector Search:** `pgvector` index (1024 dimensions, 10M capacity) mapping semantic agent memories.
- **Graph-Vector Database:** **HelixDB** (`graph-vector-database-hgi`), serving multi-hop relationship traversals at `http://localhost:6969` (Docker container).

---

## 5. Media & Creative Intelligence
Programmatic visual and voice assets.
- **Programmatic Video:** **Remotion** (`remotion-hgi`) rendered serverless-ly on AWS Lambda + S3 buckets. Compositions include: `founder-intro`, `pitch-deck`, `agent-recap`, `landing-cinematic`.
- **Image Generation:** Higgsfield APIs (`higgsfield-generate`, `higgsfield-product-photoshoot` using GPT Image 2/gpt_image_2) and Ideogram 4 (`ideogram-HGI`) serving as creative image engines.
- **Voice Synthesis:** **ElevenLabs** (`elevenlabs-multilingual-v2`) and NVIDIA voice models generating real-time voice response audio.

---

## 6. Trust & Security Layer (KAVACHA)
Policy compliance, runtime isolation, and auditing.
- **Core Framework:** **Kavacha** cybersecurity system.
- **Vulnerability Checks:** Deploys `GarudaX` (Red team, 754 cybersecurity skills, 14 MITRE tactics) and `Prahari` (Blue team, security auditing, detection, threat intel).
- **Static Scans:** Deploys `AgentShield` running 1,282 automated tests and 102 compliance rules.

---

## 7. Infrastructure & Deployment Layer
AWS cloud components (with future plans for Railway orchestration).
- **Active Infrastructure:** AWS EKS cluster `hgi-core` in `us-east-1` (running 16 pods in namespace `hgi-v5`).
- **Routing:** Route 53 pointing domains (`re-evolveon.com`, `hq.re-evolveon.com`, `api.re-evolveon.com`) to the AWS ALB.
- **Blockers for Launch:**
  1. Google & GitHub OAuth Passport strategies missing in NestJS (`apps/api`).
  2. macOS Desktop app `.dmg` installer not compiled (`npm run build:mac` not executed).
  3. Railway staging migration pending.

---
*[[../../VAULT-INDEX|← Home]]*
*[[../../06-Operations/Infrastructure/System-Registry|System Registry →]]*
