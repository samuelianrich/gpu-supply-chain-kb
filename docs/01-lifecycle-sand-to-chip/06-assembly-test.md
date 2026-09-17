# 06 — Assembly, test, and board/module integration

## What happens

### Wafer sort (front-end exit)

- Electrical test at wafer level identifies passing die (**Known Good Die**).
- For large GPU dies, sort strategies and repair (where applicable) heavily affect effective yield (**Likely**).

### Package assembly

- Die attach / bonding (already partly covered under CoWoS chip-on-wafer).
- Substrate attach, ball attach, lid / heat spreader (product-dependent).
- Marking, baking, dry-pack.

### Final test

- Package-level ATE (automated test equipment) for stuck-at, speed bins, HBM interface training, power rails.
- Burn-in / HTOL sampling for reliability qualification.
- System-level test (SLT) increasingly important for AI GPUs (**Likely** industry trend).

### Board / tray / rack (system assembly)

For NVIDIA platforms, ODMs/OEMs assemble:

- GPU baseboards / compute trays
- NVLink switch trays
- Power shelves, CDUs (coolant distribution), racks
- Cabling / blind-mate midplanes (Vera Rubin emphasizes modular cable-free trays in NVIDIA materials — **Confirmed** Technical Blog)

Partners listed for Vera Rubin availability include major clouds and OEMs (Dell, HPE, Lenovo, Supermicro, Quanta, Wistron, Foxconn, etc.) (**Confirmed**; NVIDIA Newsroom 2026-03-16).

## Key materials / inputs

- Packaged GPU / CPU / switch / NIC / DPU components
- PCBs (high-layer server boards)
- Connectors, cold plates, manifolds, quick-disconnects
- VRMs / power stages, bulk capacitors
- TIM, gap pads, EMI shields
- Firmware / BMC / security roots of trust

## Typical suppliers / regions (OSAT & system)

| Role | Examples | Notes |
|------|----------|-------|
| Foundry backend | TSMC AP | CoWoS finish |
| OSAT | ASE, Amkor, JCET, SPIL (ASE), Powertech, etc. | May handle adjacent products / older packages |
| ATE | Teradyne, Advantest | Test cell CapEx |
| ODM / OEM | Foxconn, Quanta, Wistron, Wiwynn, Inventec, Pegatron, Dell, HPE, Lenovo, Supermicro, Cisco | Rack integration |
| Cooling | Vertiv, CoolIT, nVent, OEM CDUs, etc. | Liquid cooling ecosystem (**Likely** set) |

## Process equipment classes

- Probers (wafer sort)
- Handlers / ATE
- Reflow / flux clean
- X-ray / SAT
- Board ICT / flying probe / functional SLT racks
- Liquid-cooling leak test / pressure test

## Yield / risk notes

- Late discovery of HBM lane failures is expensive (package scrap).
- Rack-scale products shift yield into **system bring-up** (NVLink training, power sequencing).
- Counterfeit / gray-market components are a tracker risk for boards (**Likely** general electronics risk).

## How this feeds a modern AI GPU

A “shippable” AI GPU for hyperscalers is often a **tray or NVL72 rack**, not a bare BGA. Test coverage must span die → package → tray → rack. NVIDIA’s Vera Rubin materials describe hot-swappable trays, NVLink resiliency, and Mission Control operational software (**Confirmed**; Technical Blog).

## Tracker signals

| Signal | Why |
|--------|-----|
| ATE lead times | Test bottleneck |
| ODM rack throughput | System ship gate |
| Liquid-cooling QD / manifold shortages | Deployability |
| SLT farm utilization at ODMs | Quality escapes vs capacity |
| Partner GA timing (H2 2026 for Vera Rubin products per NVIDIA) | Demand realization |

## Evidence & citations

- NVIDIA Newsroom ecosystem / H2 availability: https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17.
- NVIDIA Technical Blog — tray modularity, RAS, liquid cooling: https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17.

**Unknown:** Exact OSAT split (if any) outside TSMC for Rubin GPU final package test vs NVIDIA in-house / ODM SLT.
