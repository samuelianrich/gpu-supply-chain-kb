# System-level BOM — Vera Rubin NVL72 (and related racks)

Scope: **rack / POD**, not bare die. Quantities below for **one NVL72 rack** unless noted.

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |
|------|----------------|---------------------|----------|----------|-------|
| Rubin GPU package (w/ HBM4) | 72 | NVIDIA design; TSMC foundry/packaging (**Likely**); HBM: SK hynix / Samsung / Micron | Confirmed qty | NVIDIA Newsroom 2026-03-16; Tech Blog | Silicon suppliers not named by NVIDIA on newsroom page |
| Vera CPU package | 36 | NVIDIA design; foundry **Unknown**/Likely TSMC | Confirmed qty | same | Process node not Confirmed on NVIDIA pages reviewed |
| NVLink 6 switch devices | Unknown (multiple per switch tray; 36 switches in all-to-all diagram narrative) | NVIDIA | Likely / partial | Tech Blog topology figure (72 GPU ↔ 36 switches) | Exact chips-per-tray **Unknown** without datasheet |
| ConnectX-9 SuperNIC | Unknown (tray-level: quad boards; 1.6 Tb/s per GPU cited) | NVIDIA / Mellanox lineage | Confirmed capability | Tech Blog | Board count per rack **Unknown** publicly in sources reviewed |
| BlueField-4 DPU | Unknown per rack | NVIDIA | Confirmed presence | Newsroom / Tech Blog | Exact NVL72 DPU count **Unknown** |
| Spectrum-6 / Quantum scale-out | POD-level (SPX rack SKU) | NVIDIA | Confirmed as platform rack | Newsroom | Separate Spectrum-6 SPX Ethernet rack SKU |
| Compute tray (liquid-cooled) | Unknown | ODMs: Foxconn, Quanta, Wistron, etc. | Confirmed partner list | Newsroom | Tray count = f(superchips); **Unknown** exact |
| NVLink switch tray | Unknown | ODMs / NVIDIA reference | Confirmed tray type | Tech Blog | |
| CDU / liquid cooling loop | Unknown | Vertiv, CoolIT, nVent, OEM CDUs (**Likely**) | Speculative suppliers | Industry pattern | NVIDIA claims warm-water DLC lineage |
| Power shelf / busbar / PSU | Unknown | Delta, Lite-On, Bel, etc. (**Speculative**) | Unknown | — | Rack kW **Unknown** as single official number in sources reviewed |
| Vera CPU Rack (alt SKU) | 256 Vera CPUs | same CPU supply chain | Confirmed | Newsroom | Separate from NVL72 |
| Groq 3 LPX Rack | 256 LPU | Groq / NVIDIA integration | Confirmed | Newsroom | H2 2026 availability stated |
| BlueField-4 STX storage rack | Unknown | NVIDIA | Confirmed SKU | Newsroom | |
| MGX rack mechanical | 1 per rack | >80 MGX partners | Confirmed ecosystem size claim | Tech Blog / Newsroom | Third-gen MGX |

### Citations

- https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17
- https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17
