---
title: V6 Design Tokens
type: design-system
tags: [#hq-v6, #design-system, #tokens]
created: 2026-06-20
figma: FZ1SAUqktjroN1VGswyEuc
status: approved
---

# V6 Design Tokens

**Figma Source:** [RE-EVOLVE HQ V6 — Design System](https://www.figma.com/design/FZ1SAUqktjroN1VGswyEuc/)
**Status:** ✅ Approved & Implemented

## Color — Surface Hierarchy

| Token | Value | Usage |
|-------|-------|-------|
| `--v6-bg` | `#07070F` | Canvas void |
| `--v6-s1` | `#0C0C18` | Sidebar / Topbar |
| `--v6-s2` | `#111122` | Card / Panel |
| `--v6-s3` | `#181830` | Elevated / Hover |
| `--v6-s4` | `#20203C` | Active / Selected |

## Color — Brand

| Token | Value | Usage |
|-------|-------|-------|
| `--v6-accent` | `#7B61FF` | Primary CTA / Nav |
| `--v6-accent-hover` | `#9278FF` | Hover state |
| `--v6-censa` | `#A78BFF` | CENSA cognitive core |
| `--v6-data` | `#00E5FF` | Data readouts |
| `--v6-voice` | `#FF3CF7` | Voice / Mic active |

## Color — Status

| Token | Value |
|-------|-------|
| `--v6-success` | `#19D3AE` |
| `--v6-danger` | `#FF4D4D` |
| `--v6-warning` | `#F5A623` |

## Typography

| Role | Font | Size | Weight |
|------|------|------|--------|
| Page Title | Space Grotesk | 22px | 600 |
| Module H | Space Grotesk | 15px | 600 |
| Card Heading | Space Grotesk | 13px | 600 |
| Body | Inter | 14px | 400 |
| Label | Inter | 12px | 500 |
| Data XL | JetBrains Mono | 30px | 700 |
| Code | JetBrains Mono | 12px | 400 |

## Spacing

4px base unit: `4 / 8 / 12 / 16 / 20 / 24 / 32 / 48 / 64px`

## Themes

- **Dark:** "The Universe" (`data-theme="universe"`)
- **Light:** "The Future" (`data-theme="future"`)

## Implementation

- CSS: `apps/hq/app/globals.css`
- Tailwind: `apps/hq/tailwind.config.ts`

---
*[[01-HQ-V6/INDEX|← HQ V6]]*
