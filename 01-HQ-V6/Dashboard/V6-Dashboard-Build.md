---
title: V6 Intelligence Dashboard — Build Log
type: build-log
tags: [#figma, #dashboard, #v6, #hq]
created: 2026-06-20
status: in-progress
figma-file: BacP14DHobr8lPZwlGWWYD
---

# V6 Intelligence Dashboard

> Exact HQ dashboard build — pixel-accurate to reference screens, live data only, Artoies as VENTURE-001, AR-019 account.

**Figma File:** [RE-EVOLVE ON HGI — V6 Intelligence Dashboard](https://www.figma.com/design/BacP14DHobr8lPZwlGWWYD)

---

## Screens

| # | Screen | Status | Node |
|---|--------|--------|------|
| 01 | Command Center | ✅ Done | `2:2` |
| 02 | Mission Control | ✅ Done | `3:2` |
| 03 | Founder Cockpit | ✅ Done | `4:2` |
| 04 | Agent Orchestration | 🔄 Pending | — |
| 05 | Event Bus Monitor | 🔄 Pending | — |
| 06 | Economic Intelligence | 🔄 Pending | — |
| 07 | Analytics & Reports | 🔄 Pending | — |
| 08 | Emergency Protocols | 🔄 Pending | — |
| 09 | Founder Profile | 🔄 Pending | — |
| 10 | CENSA OS | 🔄 Pending | — |

---

## Design Tokens

| Token | Value | Use |
|-------|-------|-----|
| bg | `#07070F` | Page background |
| sidebar | `#080912` | Sidebar/topbar |
| card | `#080C1F` | Card backgrounds |
| accent/violet | `#7B61FF` | Primary accent |
| censa | `#A78BFF` | CENSA color |
| data/cyan | `#00E5FF` / `#17E3FF` | Data, live indicators |
| voice/magenta | `#FF3CF7` | Voice, alerts, founder |
| teal | `#19D3AE` | Health, positive states |
| gold | `#E0AD4A` | AI confidence, revenue |
| white-primary | `#E8EEFF` | Primary text |
| dim | `#4A5680` | Labels, metadata |

---

## Layout System

- **Canvas**: 1440 × 900
- **Sidebar**: 140–200px wide, dark navy, active item = cyan left accent bar
- **Topbar**: 44–48px, search left, time/status/avatar right
- **Content**: Remaining space, 8–20px padding
- **Cards**: `rgba(8,12,32,0.85)` bg, 1px border `rgba(color,0.1)`, 8–10px corner radius
- **KPI strip**: 6 equal cards, color-coded accent top line, large black metric value
- **Grid**: 3-column: visualization left (40%), activity center-right (30%), insights/panels right (30%)

---

## Accounts

- **Founder**: AR-019 · nextunicorn2026@gmail.com · RE-EVOLVE ON HGI
- **Venture**: Artoies · VENTURE-001 · research stage · internal-assessment

---

*[[../INDEX|← 01-HQ-V6]] · [[../../VAULT-INDEX|← Home]]*
