---
title: System Registry
type: operations
tags: [#operations, #system, #registry, #infrastructure]
created: 2026-06-20
updated: 2026-06-20
version: "6.0.0"
---

# 🖥️ HGI V6 System Registry

This registry provides a complete, authoritative mapping of all physical and logical software components in the **RE-EVOLVE ON HGI V6** monorepo workspace.

---

## 📦 Monorepo Workspace Root
- **Upstream Repository:** `https://github.com/nextunicorn2026/RE-EVOLVE-ON-HGI-V.0.1.git`
- **Active Branch:** `release/hgi-v5-rc1`
- **Monorepo Manager:** `pnpm@9.0.0`
- **Root Configs:** [package.json](file:///Users/nextunicorn/package.json), [pnpm-workspace.yaml](file:///Users/nextunicorn/pnpm-workspace.yaml), [turbo.json](file:///Users/nextunicorn/turbo.json)
- **Google Workspace CLI:** Installed `@googleworkspace/cli@0.22.5` (`gws` CLI tool) in the root dependencies to handle Drive, Sheets, Gmail, and Docs automation.

---

## 📱 Applications (`apps/*`)
Deployable user-facing and controller interfaces.

| Name | Directory | Tech Stack | Status | Purpose / Description |
| :--- | :--- | :--- | :--- | :--- |
| **Web** | [apps/web](file:///Users/nextunicorn/apps/web) | Next.js 14, React | ✅ Built | Marketing landing page; applies adaptive-aurora theme. |
| **HQ** | [apps/hq](file:///Users/nextunicorn/apps/hq) | Next.js 14 App Router | ✅ Built | Core Intelligence dashboard and Command Center; 58 sidebar items. |
| **API** | [apps/api](file:///Users/nextunicorn/apps/api) | NestJS | ✅ Built | Core platform API. Currently missing PassportJS Google/GitHub OAuth. |
| **Desktop** | [apps/desktop](file:///Users/nextunicorn/apps/desktop) | Electron, React | ⚠️ Code Ready | Standalone desktop shell. Version 6.0.2. Installer build is currently blocked. |
| **Mobile** | [apps/mobile](file:///Users/nextunicorn/apps/mobile) | React Native, Expo | ⏳ Planned | Mobile platform client; references TestFlight/APK build pipeline. |
| **Kavacha** | [apps/kavacha](file:///Users/nextunicorn/apps/kavacha) | Custom Security | ✅ Active | Red/Blue team monitoring and vulnerability scanner interface. |
| **AR-019** | [apps/ar019](file:///Users/nextunicorn/apps/ar019) | Node.js / Shell | ✅ Active | Founder-specific scripts, onboarding workflows, and environment controllers. |
| **Infra** | [apps/infra](file:///Users/nextunicorn/apps/infra) | Terraform, Kubernetes | ✅ Active | Infrastructure as Code configuration (EKS manifests, VPC setup). |

---

## 🛠️ Shared Packages (`packages/*`)
Reusable internal modules and SDK libraries.

| Package Name | Directory | Focus Area | Notes / Key Integrations |
| :--- | :--- | :--- | :--- |
| **agents** | [packages/agents](file:///Users/nextunicorn/packages/agents) | Agent Orchestration | Core agent civilization logic and the 24-agent Marketplace. |
| **memory** | [packages/memory](file:///Users/nextunicorn/packages/memory) | Data Layer | MemoryFabric controller: maps PostgreSQL + pgvector + HelixDB. |
| **mcp-server** | [packages/mcp-server](file:///Users/nextunicorn/packages/mcp-server) | Context Protocol | Exposes core platform tools to external consumer LLMs. |
| **orchestration** | [packages/orchestration](file:///Users/nextunicorn/packages/orchestration) | Coordination | Event fabric bus (Sarathi Prime) orchestrating agents asynchronously. |
| **cli** | [packages/cli](file:///Users/nextunicorn/packages/cli) | CLI Interface | Command line client. Features boot animation and Ora spinners. |
| **censa-routing**| [packages/censa-routing](file:///Users/nextunicorn/packages/censa-routing) | Cognitive Flow | Advanced routing and intent-mapping logic for CENSA. |
| **ui** | [packages/ui](file:///Users/nextunicorn/packages/ui) | Design System | `@hgi/ui` v2 design system component library. ThemeProviderV2. |
| **three** | [packages/three](file:///Users/nextunicorn/packages/three) | WebGL Graphics | ThreeJS/Fiber/Drei canvas configurations for interactive 3D UI. |
| **deployment** | [packages/deployment](file:///Users/nextunicorn/packages/deployment) | CI/CD | Compilation and containerization scripts for deployment pipelines. |
| **config** | [packages/config](file:///Users/nextunicorn/packages/config) | Environment | Shared compilation, tsconfig paths, and environment settings. |

---

## 🧠 Microservices (`services/*`)
Supporting backend runtimes running concurrently in the EKS namespace.

1. **agent-registry-service:** Deploys and inventories custom agent definitions.
2. **ai-agent-service:** Agent runtime worker pool for executing text, research, and coding tasks.
3. **api-gateway:** Reverse-proxy routing external requests to correct internal microservices.
4. **approval-service:** Manages human-in-the-loop authorization workflows.
5. **audit-service:** Captures audit records and records state modifications.
6. **auth-service:** Issues and decrypts security tokens.
7. **automation:** n8n-backed trigger-action automation engine.
8. **github-intelligence-service:** Scans repositories for structural patterns and imports components.
9. **governance-service:** Enforces security and policy rules.
10. **incubation-service:** Manages venture lifecycle events.
11. **kavacha-api:** Exposes penetration testing and vulnerability stats.
12. **llm-gateway:** Dynamic routing to lowest-cost LLM backends (FreeLLM API).
13. **memory:** Vector storage and query endpoints.
14. **orchestration-service:** Controls running LangGraph and event workflows.
15. **policy-service:** Compiles and enforces OPA rule trees.
16. **re-evolve-hq-backend:** Backend controllers powering the HQ dashboard.
17. **realtime-service:** WebSockets routing streaming voice, metrics, and chat.
18. **user-hq-backend:** Workspace-scoped user operations.
19. **voice:** Voice-to-text, text-to-voice (ElevenLabs, NVIDIA services) endpoint.
20. **workspace-steward:** Automates environment synchronization, logging, and metrics.

---

## 🌐 Network Domain Mapping

| Domain | Surface Path | Current Environment | Production Destination |
| :--- | :--- | :--- | :--- |
| `re-evolveon.com` | `apps/web` | Active on EKS (namespace `hgi-v5`) | Target: Railway Custom Domain |
| `hq.re-evolveon.com` | `apps/hq` | Active on EKS (namespace `hgi-v5`) | Target: Railway Custom Domain |
| `api.re-evolveon.com` | `apps/api` | Active on EKS (namespace `hgi-v5`) | Target: Railway Custom Domain |
| `beta.re-evolveon.com` | `apps/ar019` | Inactive | Target: Railway Custom Domain |

---
*[[../../VAULT-INDEX|← Home]]*
