# Build and Test

**Project:** `DCI_VTON`
**Upstream:** https://github.com/KiseKloset/DCI-VTON
**License:** Apache 2.0

## Quick Start

```bash
git clone https://github.com/KiseKloset/DCI-VTON
cd DCI-VTON
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B local virtual try-on and style recommendation
2. AIOSS inventory and transaction audit chain
3. AES-256 encryption for all customer data and purchase history
4. Single-binary retail management system with no cloud dependency
5. Zero-cloud: all AI features run locally on store hardware
6. GPU/CPU equalizer: try-on inference on GPU when available, CPU otherwise
7. Zero-telemetry: removes all third-party tracking pixels
8. Open size chart API: standard body measurement exchange format

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Primary inference task: <5s on CPU, <1s on GPU |
| Throughput | Batch processing: >100 items/hour on single CPU server |
| Memory | <8GB RAM for standard deployment |
| Accuracy | Task-specific accuracy within 5% of cloud-API baseline |

## Build Status

Not yet measured. Run verified build and record actual figures above.
