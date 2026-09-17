# 02 — Crystal ingot growth and wafering (200mm / 300mm)

## What happens

1. EG polysilicon is melted in a fused-quartz crucible.
2. **Czochralski (CZ)** growth pulls a single-crystal **ingot** (boule), doped as specified (e.g., boron/phosphorus for substrate resistivity).
3. Ingot is cropped, ground, notched/flatted, and **sliced** into wafers (wire saw).
4. Wafers are lapped, etched, **polished** (and often epitaxial layers grown for logic) to meet flatness, particles, and crystal defect specs.
5. Ship as **prime** 200mm or **300mm** wafers to foundries/IDMs.

Leading-edge logic for AI GPUs is overwhelmingly **300mm** (**Confirmed**; SEMI wafer shipment statistics context via OECD 2025 value-chain paper citing SEMI).

## Key materials / inputs

- EG polysilicon
- Fused-quartz crucibles (HPQ-derived)
- Dopants
- Slurry / chemicals for slicing and CMP-prep polishing
- Ultra-pure water (UPW) and cleanroom infrastructure

## Typical suppliers / regions (named where known)

Silicon wafer supply is an oligopoly:

| Supplier | HQ / core region | Role |
|----------|------------------|------|
| Shin-Etsu Handotai (Shin-Etsu Chemical) | Japan | Leading 300mm share (**Estimated** ~40%+ in 2024 secondary summaries; confirm annually via SEMI/vendor IR) |
| SUMCO | Japan | #2 class wafer maker |
| GlobalWafers | Taiwan | Major 300mm supplier |
| Siltronic | Germany | Major supplier |
| SK Siltron | South Korea | Major supplier |

(**Likely** concentration of top suppliers controlling majority share; exact % fluctuate—cite SEMI or company IR before using a number in tracker dashboards.)

OECD notes high concentration and trade dependencies for silicon wafers (**Confirmed**; OECD 2025).

## Process equipment classes

- CZ pullers
- Multi-wire saws
- Grinders / edge polishers
- CMP polishers for wafer finishing
- Epitaxial reactors (epi wafers for many logic flows)
- Metrology: flatness, nanotopography, particles, resistivity

## Yield / risk notes

- **Crystal defects** (COP, dislocations, oxygen precipitates) affect device yield downstream.
- **300mm capacity expansion** takes years and large CapEx; not a short-cycle response to AI demand spikes (**Likely**; structural industry fact—confirm with wafer-maker CapEx commentary).
- **200mm** remains critical for analog, power, MCU, and many specialty chips that appear on GPU *boards* (PMICs, etc.) even when the GPU logic die is 300mm (**Likely**).

## How this feeds a modern AI GPU

- Logic compute dies and I/O dies: 300mm foundry wafers.
- HBM: DRAM wafers from memory IDMs (also 300mm class for leading HBM).
- Interposer (CoWoS-S): additional silicon wafers consumed as passive interconnect—raising silicon intensity per shipped GPU package (**Likely** for CoWoS-S; CoWoS-L reduces large monolithic interposer need—see packaging doc).

## Tracker signals

| Signal | Why |
|--------|-----|
| SEMI monthly silicon wafer shipments | Demand lagging indicator |
| Wafer ASP / long-term agreements | Margin & allocation |
| Japan earthquake / energy risk near Shin-Etsu/SUMCO fabs | Geographic concentration |
| Epi capacity for advanced logic | Leading-edge readiness |

## Evidence & citations

- OECD (2025), *Mapping the semiconductor value chain* (polysilicon → wafer; SEMI wafer shipment cite): https://www.oecd.org/content/dam/oecd/en/publications/reports/2025/06/mapping-the-semiconductor-value-chain_5ba52971/4154cdbf-en.pdf — accessed 2026-09-17.
- Secondary market-structure summaries (use cautiously): e.g., SEMI VISTA / industry blogs on Shin-Etsu share — treat %-share as **Estimated** until SEMI primary table attached.
- USGS Silicon MCS (polysilicon → semiconductor grades): https://pubs.usgs.gov/periodicals/mcs2026/mcs2026-silicon.pdf — accessed 2026-09-17.

**Unknown:** Exact wafer starts per Rubin GPU package (depends on die size, multi-die count, yield, and interposer type)—needs die-area disclosure + yield model.
