# Educators — DCI_VTON

**Project:** DCI_VTON  
**Category:** CLOTHING_RETAIL  
**Upstream:** see BENCH.json  
**Pinned commit:** `5baa6d14b96022443a8beeda147c5da6013b573c`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f0497ff993769222ea5dff3c22dcf583e8ae24fd4d2d9619127a9634e8606922`  
**Date:** October 2026

## Teaching with DCI_VTON

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `f0497ff993769222ea5dff3c22dcf583e8ae24fd4d2d9619127a9634e8606922` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
