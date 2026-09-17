# 01 — Quartz, metallurgical silicon, and polysilicon

## What happens

Semiconductor logic starts as **silica** (SiO₂), typically from quartzite or high-purity quartz (HPQ), not generic beach sand—though popular accounts often say “sand.”

1. **Mining / beneficiation** of quartzite or HPQ.
2. **Carbothermic reduction** in submerged-arc furnaces → **metallurgical-grade silicon (MG-Si)** (~98–99% Si).
3. **Chemical purification** (commonly Siemens / hydrochlorination routes involving trichlorosilane) → **polysilicon** rods or chunks.
4. Grade split:
   - **Solar-grade** polysilicon (still high purity; volume-driven).
   - **Electronic-grade (EG)** polysilicon for semiconductor crystal growth (ultra-high purity; fewer producers qualify).

EG polysilicon becomes the feedstock for Czochralski (CZ) single-crystal ingots used for most logic wafers (**Confirmed** process chain in OECD semiconductor value-chain mapping and USGS silicon commodity notes; see citations below).

## Key materials / inputs

| Input | Role | Notes |
|-------|------|-------|
| Quartzite / silica | Silicon source | Abundant globally (**Confirmed**; USGS) |
| High-purity quartz (HPQ) | Fused-quartz crucibles for CZ growth | Tight geography; critical for wafering upstream (**Confirmed**; USGS quartz MCS) |
| Carbon reductants | MG-Si furnace chemistry | Process industry input |
| Chlorosilanes / HCl | Polysilicon purification chemistry | Specialty chemical plants |
| Electricity | Energy-intensive reduction & CVD | Regional cost & ESG factor |

## Typical suppliers / regions

- **HPQ:** United States historically important (e.g., Spruce Pine, NC area discussed in USGS quartz summaries); other sources include Australia, Brazil, Canada, China, India, Russia (**Confirmed**; USGS Mineral Commodity Summaries — Quartz crystal / HPQ notes).
- **Silicon metal / MG-Si:** Multiple countries; China is a major producer of silicon materials in USGS world pictures (**Confirmed**/context; USGS Silicon MCS 2025–2026).
- **Polysilicon (EG):** Small set of qualified producers. USGS notes a handful of U.S. polysilicon producers and ongoing quality/volume qualification challenges for some facilities (**Confirmed**; USGS Silicon MCS 2026). Global EG capacity is concentrated among specialized chemical/semiconductor materials firms (names and exact share tables vary by year—treat market-share % as **Estimated** unless from SEMI/primary IR).

## Process equipment classes

- Mining / crushing / flotation for silica.
- Submerged-arc furnaces (MG-Si).
- Chemical plants: hydrochlorination, distillation trains, Siemens CVD reactors for polysilicon rods.
- Clean handling for EG product.

## Yield / risk notes

- **Purity yield:** Parts-per-billion contamination can disqualify EG lots; solar and EG are not freely interchangeable without requalification (**Likely**; industry process consensus—confirm with producer specs).
- **HPQ / crucible risk:** USGS links growth in silicon ingot manufacturing (PV + semiconductor) to HPQ demand for fused-quartz crucibles (**Confirmed**; USGS quartz MCS 2025). Storm or mine outages at concentrated HPQ sites are a classic tracker signal.
- **Trade / tariffs:** Silicon metal and polysilicon trade flows are geopolitically sensitive; USGS discusses import dynamics and policy context (**Confirmed** as reported trends; magnitudes year-specific).

## How this feeds a modern AI GPU

Without EG polysilicon → no 300mm wafers → no TSMC (or other) logic dies → no CoWoS package with HBM. AI GPUs do not “see” MG-Si directly, but **EG polysilicon + HPQ crucibles** are foundational. HBM DRAM also depends on the same wafer/polysilicon ecosystem (memory fabs), so AI packages stress **both** logic and memory silicon supply chains.

## Tracker signals

| Signal | Why watch | Typical source |
|--------|-----------|----------------|
| HPQ mine / crucible outages | Gates CZ capacity | USGS events; producer notices |
| EG polysilicon spot / contract | Cost & allocation | Producer IR; trade press (**Estimated** prices) |
| China vs non-China EG share | Diversification | USGS / SEMI / OECD |
| Energy prices in MG-Si regions | Cost shock | Commodity desks |

## Evidence & citations

- USGS, *Mineral Commodity Summaries — Silicon* (2025 and 2026 editions): polysilicon production notes, silicon metal uses. https://pubs.usgs.gov/periodicals/mcs2026/mcs2026-silicon.pdf and https://pubs.usgs.gov/periodicals/mcs2025/mcs2025-silicon.pdf — accessed 2026-09-17.
- USGS, *Mineral Commodity Summaries — Quartz Crystal* / HPQ demand for crucibles (2025): https://pubs.usgs.gov/periodicals/mcs2025/mcs2025-quartz.pdf — accessed 2026-09-17.
- USGS Silica statistics hub: https://www.usgs.gov/centers/national-minerals-information-center/silica-statistics-and-information — accessed 2026-09-17.
- OECD (2025), *Mapping the semiconductor value chain*: quartz → polysilicon → wafer narrative. https://www.oecd.org/content/dam/oecd/en/publications/reports/2025/06/mapping-the-semiconductor-value-chain_5ba52971/4154cdbf-en.pdf — accessed 2026-09-17.

**Unknown:** Exact EG polysilicon tonnage consumed per leading-edge AI GPU wafer start (would need foundry wafer-spec + mass-balance study).
