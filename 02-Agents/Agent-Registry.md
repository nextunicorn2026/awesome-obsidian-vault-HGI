---
title: Agent Registry
type: agents
tags: [#agent, #registry, #civilization, #marketplace]
created: 2026-06-20
updated: 2026-06-20
version: "6.0.0"
---

# 🤖 HGI V6 Agent Registry

This registry catalogues the **8 core agent civilizations** and the **24-agent Marketplace** built into the RE-EVOLVE ON HGI V6 platform.

---

## 🏛️ The Eight Agent Civilizations

The sovereign operating layers that control and maintain the ecosystem.

| Codename | Civilization | Primary Role | Psychology / Alignment | Preferred Model | Registry Path | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **HGI-X01** | **CENSA** | Sovereign Intelligence Layer | AWE + CONTROL | Claude 3.5 Sonnet | [censa/censa.service.ts](file:///Users/nextunicorn/apps/api/src/censa/censa.service.ts) | ✅ Deployed |
| **HGI-A01** | **SAROS** | Strategic Orchestration (SARATHI) | MOMENTUM + AWARENESS | Claude 3.5 Sonnet / GPT-4o | [supreme/sarathi-prime.ts](file:///Users/nextunicorn/packages/agents/src/supreme/sarathi-prime.ts) | ✅ Deployed |
| **HGI-A03** | **NEXUS** | Research & Web Intelligence | EXPLORATORY + ANALYTICAL | DeepSeek R1 / Claude Sonnet | [supreme/atlas-grid.ts](file:///Users/nextunicorn/packages/agents/src/supreme/atlas-grid.ts) | ✅ Deployed |
| **VANTIS CORE** | **VANTIS** | Venture Strategy & Valuation | PURPOSE + UTILITY | GPT-4o / Claude Sonnet | [agents/VANTIS-Overview](file:///Users/nextunicorn/HGI-Vault/02-Agents/VANTIS/VANTIS-Overview.md) | 🔄 In Progress |
| **FORGE CORE** | **FORGE** | Code Execution & Devops | PRECISION + SPEED | Qwen Coder / Claude Sonnet | [agents/FORGE-Overview](file:///Users/nextunicorn/HGI-Vault/02-Agents/FORGE/FORGE-Overview.md) | 🔄 In Progress |
| **NOVA CORE** | **NOVA** | Visual Design & Motion System | CREATION + PARITY | Qwen Vision / Claude Sonnet | [agents/NOVA-Overview](file:///Users/nextunicorn/HGI-Vault/02-Agents/NOVA/NOVA-Overview.md) | 🔄 In Progress |
| **LUMEN CORE** | **LUMEN** | Knowledge Universe & Docs | SYNTHESIS + TRUTH | Claude Sonnet / GPT-4o-mini | [agents/LUMEN-Overview](file:///Users/nextunicorn/HGI-Vault/02-Agents/LUMEN/LUMEN-Overview.md) | 🔄 In Progress |
| **HGI-A02** | **AEGIS** | Trust, Security & Compliance | TRUST + ANTI-DRIFT | AWS Titan / Claude Sonnet | [supreme/aegis-core.ts](file:///Users/nextunicorn/packages/agents/src/supreme/aegis-core.ts) | 🔄 In Progress |

---

## 🛒 The Agent Marketplace Catalog
Consolidated from **ECC-HGI** (63 agents, 251 skills) and **HGI-Native** agents. Divided into 8 categories (18 Live, 4 Partial, 2 Blueprint).

### 1. Research & Intelligence
- **Web Crawler (partial):** Rust crawler (Spider) running 4 MCP tools (`spider_scrape`, `spider_crawl`, `spider_links`, `spider_transform`).
- **Platform Researcher (live):** Authenticates to 12+ channels via `Agent-Reach` (Reddit, RSS, Exa search, YouTube, GitHub, Twitter).
- **ECC Research Agent (live):** Standard deep OSINT search with sequential thinking, Exa, and GitHub integration.
- **Google Workspace Assistant (live):** Dynamically automates Google Workspace operations (Drive, Sheets, Gmail, Docs, Calendar) via the `gws` CLI under tools `gws.execute`, `gws.schema`, and `gws.command`.

### 2. Development & Engineering
- **Code Reviewer (live):** Multi-dimension code review (correctness, security vulnerability check, performance overhead scan).
- **TDD Guide (live):** Asserts test-driven implementations (unit tests, chaos tests, E2E integrations).
- **Architect (live):** System design templates, ADR validation, technical debt analysis.

### 3. Security & Compliance
- **Kavacha Red Team (live):** `GarudaX` scanner (754 cybersecurity skills, 185+ penetration tools, 14 MITRE tactics).
- **Kavacha Blue Team (live):** `Prahari` threat detection and environment hardening engine.
- **ECC Security Auditor (live):** `AgentShield` rules runner (1,282 security asserts, 102 rules).

### 4. Content & Media
- **Video Generator (partial):** **Remotion** framework executing video layouts (founder pitch, landing cinematic) rendered on AWS Lambda + S3.
- **ContentPrime (live):** Native copy, brand voice formatting, social media campaigns planner.
- **Doc Generator (live):** Auto-compiles markdown files (API documents, README, changelogs) from source trees.

### 5. Sales & Revenue
- **RevenuePrime (live):** Pipeline metric analysis, deal score predictor, time-series forecasting.
- **CRMPrime (live):** Contact enrichment and automated sequence triggers.
- **PartnershipPrime (live):** Sourcing outreach candidates and structuring contracts.

### 6. Operations & DevOps
- **DevOps Engineer (live):** Deploys Terraform layouts, edits Kubernetes YAMLs, and adjusts GitHub action workflows.
- **SRE Agent (live):** Outage alert runbook executor, cost reduction analyzer.
- **SanjeevaniX (live):** Custom self-healing and recovery script monitor; triggers fallback gateways on failure.

### 7. Data & Analytics
- **ML Engineer (live):** Custom pipeline optimization and model evaluation evaluator.
- **Graph Memory Analyst (partial):** HelixDB graph traversal and vector mapping analyst.
- **Data Scientist (live):** Explains data distributions, runs statistical hypotheses, outputs diagrams.

### 8. Communication & Outreach
- **AlterSend P2P (blueprint):** Encrypted serverless peer-to-peer file transfer agent. Needs altersend REST shim completed.
- **GrowthPrime (live):** Identifies growth hacks, sets up activation funnels and A/B test criteria.
- **CallPrime (live):** Voice transcription, dialogue analysis, sentiment analysis.

---
*[[../VAULT-INDEX|← Home]]*
*[[../00-Foundation/Architecture/Architecture-Registry|Architecture Registry →]]*
