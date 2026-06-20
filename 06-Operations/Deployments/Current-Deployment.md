---
title: Current Deployment Status
type: operations
tags: [#operations, #deployment, #infrastructure]
created: 2026-06-20
updated: 2026-06-20
---

# Current Deployment Status

**Last Updated:** 2026-06-20
**Environment:** Production

## Infrastructure

| Component | Value |
|-----------|-------|
| Cloud | AWS EKS |
| Cluster | `hgi-core` |
| Region | `us-east-1` |
| Account | `987569578681` |
| Namespace | `hgi-v5` |
| Domain | `re-evolveon.com` |

## Pod Status (hgi-v5)

| Service | Replicas | Status |
|---------|---------|--------|
| hgi-api-v5 | 3 | ✅ Running |
| hgi-hq-v5 | 3 | ✅ Running |
| hgi-web-v5 | 3 | ✅ Running |
| hgi-ai-agent-v5 | 3 | ✅ Running |
| hgi-ar019-v5 | 2 | ✅ Running |
| hgi-freellmapi-v5 | 1 | ✅ Running |
| hgi-voice-v5 | 1 | ✅ Running |
| **Total** | **16/16** | ✅ **All Running** |

## Active Branch

`release/hgi-v5-rc1`

## V6 Deployment Path

1. `git push origin release/hgi-v5-rc1`
2. Trigger CodeBuild (`buildspec.yml`) → builds `:v6` images → kubectl rolling update
3. Add API keys to `hgi-secrets`
4. `kubectl rollout status deployment/hgi-api-v5 -n hgi-v5`

## Environment Keys Needed for V6

- `IDEOGRAM_API_KEY` — Image generation
- `NVIDIA_API_KEY` — Video / Media generation
- `GEMINI_API_KEY` — Multimodal editing

---
*[[06-Operations/INDEX|← Operations]]*
