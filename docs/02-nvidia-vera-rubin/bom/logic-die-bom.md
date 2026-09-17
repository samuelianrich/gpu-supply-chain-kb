# Logic-die BOM — chip-level (inside packages)

Scope: **silicon dies**, not full racks.

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |
|------|----------------|---------------------|----------|----------|-------|
| Rubin GPU compute die | 2 per GPU package | TSMC (**Likely**) | Confirmed die count | Tech Blog vs Blackwell table | Node string **Unknown** on NVIDIA primary pages reviewed |
| Rubin I/O / other die | Unknown | TSMC (**Likely**) | Speculative | Secondary press (chiplet / I/O die narratives) | Barrack AI / similar claim 2 I/O dies — **Speculative** until primary |
| Vera CPU compute die | 1 monolithic (NVIDIA describes single monolithic compute die + SCF) | TSMC (**Likely**) | Likely / Confirmed monolithic narrative | Tech Blog | Node **Unknown** |
| NVLink 6 switch ASIC | ≥1 per switch chip instance | TSMC or other (**Unknown**) | Confirmed product exists | Tech Blog / Newsroom | Foundry **Unknown** |
| ConnectX-9 controller | 1 per device | NVIDIA | Confirmed | Tech Blog | |
| BlueField-4 (Grace CPU die + ConnectX-9) | dual-die package | NVIDIA / foundry mix **Unknown** | Confirmed dual-die description | Tech Blog | BF4 uses 64-core Grace CPU block |
| Spectrum-6 switch ASIC | 1 per switch chip | NVIDIA / foundry **Unknown** | Confirmed | Newsroom / Tech Blog | CPO optics engines separate |
| Photomasks / reticles | Unknown | DNP, Hoya, Photronics, etc. (**Likely**) | Speculative vendors | Industry pattern | |
| Transistor count Rubin | 336B (full chip) | — | Confirmed | Tech Blog | Not a BOM line; tracking metric |
| Transistor count Vera | 227B (secondary) / not always on NVIDIA table | — | Likely (secondary) | Secondary architecture pages | Prefer NVIDIA primary if republished |

**Unknown that would unlock this BOM:** NVIDIA or TSMC slide naming process node per die (N3P vs N3E vs other) and whether I/O dies exist on Rubin.
