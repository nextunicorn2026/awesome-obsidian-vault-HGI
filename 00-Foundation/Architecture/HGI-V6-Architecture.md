---
title: HGI V6 Architecture
type: architecture
tags: [#architecture, #v6, #foundation]
created: 2026-06-20
version: "6.0.1"
---

# HGI V6 Architecture

## Platform Surfaces

| Surface | Stack | Port | Status |
|---------|-------|------|--------|
| `apps/web` | Next.js | :3000 | Live |
| `apps/hq` | Next.js | :3002 | Live |
| `apps/api` | NestJS | :4000 | Live |
| `apps/desktop` | Electron | — | v6.0.0 |
| `apps/mobile` | — | — | Planned |

## Infrastructure

- **Cloud:** AWS EKS (`hgi-core`, us-east-1)
- **Account:** 987569578681
- **Namespace:** `hgi-v5` (live), `hgi-v6` (pending)
- **Domain:** re-evolveon.com
- **Pods:** 16/16 Running

## API Modules (55+)

Key modules:
- `auth` — JWT + Google OAuth + SAML SSO
- `censa` — CENSA cognitive operating layer
- `agents` / `agent-swarm` — Multi-agent orchestration
- `quantum-layer` — 6 RAG modes + planning + simulation
- `media` — Image / Avatar / Video generation
- `evolution-ledger` — Self-evolution tracking
- `governance-engine` — Human-governed compliance

## V6 Additions

- Phase 2: Media Engine (`/media/image|avatar|video|content`)
- Phase 3: Quantum Layer (`/quantum/status|memory|plan|simulate`)
- Phase 4: HQ V6 Screens (Media Studio, Quantum Layer)
- Phase 5: Brand unification — "Where The Cosmos Codes Itself"

## Related

- [[00-Foundation/Decisions/INDEX|Architecture Decisions]]
- [[01-HQ-V6/Design-System/V6-Tokens|V6 Design System]]
- [[06-Operations/Deployments/Current-Deployment|Deployment Status]]

---
*[[00-Foundation/INDEX|← Foundation]]*
