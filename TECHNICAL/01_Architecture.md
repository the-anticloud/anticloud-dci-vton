# Technical Architecture — DCI_VTON

**Upstream:** [https://github.com/KiseKloset/DCI-VTON](https://github.com/KiseKloset/DCI-VTON)
**License:** Apache 2.0
**Category:** CLOTHING_RETAIL
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Virtual try-on with diffusion

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local virtual try-on and style recommendation
2. AIOSS inventory and transaction audit chain
3. AES-256 encryption for all customer data and purchase history
4. Single-binary retail management system with no cloud dependency
5. Zero-cloud: all AI features run locally on store hardware
6. GPU/CPU equalizer: try-on inference on GPU when available, CPU otherwise
7. Zero-telemetry: removes all third-party tracking pixels
8. Open size chart API: standard body measurement exchange format

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_dci_vton.spec` or `go build -o dci_vton`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |