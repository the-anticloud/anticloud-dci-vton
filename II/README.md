# Independent Insurance — DCI_VTON

**Project:** DCI_VTON  
**Category:** CLOTHING_RETAIL  
**Upstream:** see BENCH.json  
**Pinned commit:** `5baa6d14b96022443a8beeda147c5da6013b573c`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f0497ff993769222ea5dff3c22dcf583e8ae24fd4d2d9619127a9634e8606922`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | DCI_VTON with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `f0497ff993769222ea5dff3c22dcf583e8ae24fd4d2d9619127a9634e8606922`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
