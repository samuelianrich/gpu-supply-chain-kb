# 03 — Front-end fab (FEOL / BEOL): making the logic die

## What happens

A blank 300mm wafer enters a **fab**. Hundreds to >1000 process steps pattern transistors and interconnects.

### FEOL (front-end-of-line)

Forms transistors and isolation:

- Cleaning / surface prep
- Oxidation / thin films
- **Photolithography** (pattern transfer)
- **Etch** (plasma / wet)
- **Ion implant** + anneal (doping)
- **Deposition** (CVD, ALD, epitaxy)
- **CMP** (chemical-mechanical planarization)
- Gate stack / FinFET or GAA transistor modules at leading edge

### BEOL (back-end-of-line)

Forms metal interconnect stack:

- Dual damascene Cu (and increasingly Co/Ru liners, etc., by node)
- Low-k / ultra-low-k dielectrics
- Many metal layers (count is node- and product-specific — **Unknown** unless disclosed)
- Passivation / bonding pads / bump prep for packaging

### Foundry vs IDM

| Model | Who designs | Who fabs | AI GPU relevance |
|-------|-------------|----------|------------------|
| **Foundry** (e.g., TSMC, Samsung Foundry) | Fabless customer (NVIDIA) | Foundry | Dominant for NVIDIA GPUs (**Confirmed** historically via NVIDIA 10-K manufacturing reliance language; node details per product vary) |
| **IDM** (e.g., Intel, Samsung LSI, memory makers) | Integrated | Own fabs | Memory HBM is IDM; some accelerators are IDM |

NVIDIA’s SEC disclosures emphasize reliance on third parties to manufacture, assemble, package, and test products (**Confirmed**; forward-looking risk language in NVIDIA Vera Rubin newsroom release / 10-K pattern).

## Lithography: EUV vs DUV at leading edge

| Tool class | Wavelength / role | Supplier posture |
|------------|-------------------|------------------|
| **EUV** | 13.5 nm; critical fine layers at advanced nodes | **ASML** sole volume EUV scanner supplier (**Confirmed** industry consensus / OECD & industry bottleneck atlases) |
| **DUV immersion (ArFi)** | Workhorse for many layers even at “EUV nodes” | ASML dominant; Nikon also present historically (**Likely**) |
| **High-NA EUV** | Next density step; limited early tools | ASML + Zeiss optics ecosystem (**Likely** for roadmap; tool counts **Estimated**) |

**Important:** Shipping a chip “on 3nm” still uses **many DUV layers**; EUV does not replace all lithography (**Confirmed** process reality in industry literature).

## Process equipment classes (major)

| Step | Equipment class | Example vendors (illustrative) |
|------|-----------------|--------------------------------|
| Lithography | Scanners / tracks | ASML; Tokyo Electron (coater/developer) |
| Etch | Conductor / dielectric etchers | Lam Research, Tokyo Electron, Applied Materials |
| Deposition | CVD / PVD / ALD / epi | Applied Materials, Lam, TEL, ASM International |
| Implant | High-current / high-energy implanters | Applied Materials, Axcelis, others |
| CMP | Polishers + slurry | Applied Materials, Ebara; slurry: Cabot, etc. |
| Metrology / inspection | CD-SEM, overlay, optical inspection, e-beam | KLA, ASML (YieldStar), Hitachi, etc. |
| Wet clean | Wet benches / single-wafer clean | TEL, Screen, others |

Vendor lists are **Likely** market leaders by segment; exact tool-of-record at TSMC N3 for NVIDIA is **Unknown** publicly.

## Yield / risk notes

- **Defect density** dominates economics of large GPU dies (near-reticle compute tiles amplify kill defects).
- **Multi-die packages** (e.g., two compute dies) shift some yield burden to packaging KGD strategy (**Likely**).
- **Export controls** on advanced tools/nodes can reshuffle geography of capacity (**Confirmed** as a policy risk category; specific license outcomes are case-by-case).

## How this feeds a modern AI GPU

Front-end produces:

- GPU compute dies
- Optional I/O / SRAM / bridge dies (product-dependent)
- CPU dies (Vera) on their own masks/flows
- Switch / NIC / DPU silicon on various nodes (not always leading-edge)

Those dies then enter **advanced packaging** with HBM—not a classic single-chip QFN path.

## Tracker signals

| Signal | Why |
|--------|-----|
| Foundry CapEx & wafer ASP by node | Capacity & pricing |
| ASML EUV shipments / backlog | Tool constraint |
| TSMC utilization commentary on HPC | AI mix |
| Export-control entity lists | Geographic risk |
| Mask / photomask blank lead times | Tapeout velocity |

## Evidence & citations

- NVIDIA Newsroom (2026-03-16), Vera Rubin platform — manufacturing third-party reliance in risk language: https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17.
- OECD (2025) semiconductor value-chain mapping (equipment & wafer dependencies): https://www.oecd.org/content/dam/oecd/en/publications/reports/2025/06/mapping-the-semiconductor-value-chain_5ba52971/4154cdbf-en.pdf — accessed 2026-09-17.
- Industry bottleneck summaries naming ASML sole-source EUV (secondary; corroborate with ASML annual report): e.g., SemiconductorX bottleneck atlas — treat sole-source role as **Confirmed** industry fact, numeric tool capacities as **Estimated**.

**Unknown:** Official NVIDIA-published process node string for every Vera Rubin die (GPU vs CPU vs switch may differ). See Vera Rubin TSMC doc for rumor vs confirmed split.
