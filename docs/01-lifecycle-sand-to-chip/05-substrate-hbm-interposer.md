# 05 — Substrates, HBM stacks, and interposers / bridges

## What happens

Three distinct supply chains converge at advanced packaging:

### A. HBM (High Bandwidth Memory)

DRAM makers build **3D-stacked DRAM** with a logic/base die and TSVs, sold as stacks that sit beside the GPU on the interposer/RDL.

Generations relevant to AI GPUs:

- **HBM3E** — volume workhorse into mid-2020s
- **HBM4** — next gen; NVIDIA Rubin publicly pairs with HBM4 (**Confirmed**; NVIDIA Technical Blog / NVL72 specs)

Major suppliers: **SK hynix**, **Samsung**, **Micron** (**Confirmed** as the three HBM vendors in industry coverage; qualification status per customer is time-varying).

### B. Silicon interposer or local bridges

- **CoWoS-S:** large silicon interposer redistributes signals between logic and HBM.
- **CoWoS-L:** smaller **local silicon interconnect** bridges plus organic RDL to span multi-reticle assemblies (**Likely** description per industry packaging analyses).

### C. Organic package substrate (ABF FC-BGA)

Beneath the interposer/RDL assembly sits a **high-layer-count organic substrate** using **Ajinomoto Build-up Film (ABF)** as the critical dielectric film for advanced flip-chip BGAs (**Confirmed**/near-sole-source role widely reported; Ajinomoto IR discusses ABF as interlayer insulating material for logic IC package substrates).

Substrate fabricators (examples): Unimicron, Ibiden, Shinko, Nan Ya PCB, Samsung Electro-Mechanics, AT&S (**Likely** leading set per Tom’s Hardware 2026 substrate survey).

## Key materials / inputs

| Item | Upstream dependency |
|------|---------------------|
| HBM stacks | DRAM wafers, TSV, bonding, advanced packaging at memory IDM |
| Interposer Si | Extra 300mm wafers + TSV process |
| LSI bridges | Small Si dies + fine interconnect |
| ABF film | Ajinomoto Fine-Techno varnish → film |
| Copper / glass cloth / other laminate | Substrate makers |
| Solder bumps / balls | Materials suppliers |

## Typical suppliers / regions

| Segment | Suppliers | Geography |
|---------|-----------|-----------|
| HBM | SK hynix, Samsung, Micron | Korea, Korea, US/JP/SG footprint mixed |
| ABF film | Ajinomoto (dominant) | Japan |
| Substrates | Unimicron (TW), Ibiden (JP), Shinko (JP), others | TW / JP / KR / EU |
| Interposer fab | Often TSMC flow | Taiwan |

## Process equipment classes

- DRAM fab tools (similar classes to logic, different recipes)
- TSV etch/fill, wafer bonding for HBM
- Substrate: laser drill, plating, ABF lamination, patterning, AOI
- Incoming Q&A: TDR, warpage metrology

## Yield / risk notes

- HBM **qualification** is customer- and generation-specific; dual-sourcing is slow (**Likely**).
- ABF and large substrates were historical bottlenecks for CPUs/GPUs; 2026 coverage describes renewed CapEx at Ibiden/Unimicron/SEMCO (**Estimated** CapEx figures in press).
- Interposer area scales poorly; drives CoWoS-L adoption narratives (**Likely**).

## How this feeds a modern AI GPU

For Rubin-class packages, public NVIDIA specs cite **up to 288 GB HBM4** and **22 TB/s** per GPU (**Confirmed**; NVIDIA Developer Blog / NVL72 product tables). Stack count is commonly discussed as **8 stacks** in secondary architecture writeups (**Likely**; confirm against official datasheet line items when publishing BOM qty).

Substrate quality gates signal integrity for HBM and SerDes escaping the package.

## Tracker signals

| Signal | Why |
|--------|-----|
| HBM supplier earnings (ASP, sold-out commentary) | Memory gate |
| NVIDIA HBM qualification matrix (3 vendors) | Dual-source health |
| Ajinomoto ABF CapEx / varnish plants | Film availability |
| Substrate lead times / layer counts for AI | Package gate |
| HBM4 12-hi vs 8-hi mix | Capacity vs bandwidth trade |

## Evidence & citations

- NVIDIA HBM4 on Rubin (**Confirmed**): https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17; also NVL72 product page tables.
- Ajinomoto electronic materials / ABF strategy PDF: https://www.ajinomoto.co.jp/company/en/ir/event/business_briefing/main/011117/teaserItems1/01/linkList/03/link/20260630_presentation_E.pdf — accessed 2026-09-17.
- Tom’s Hardware (2026) ABF substrate industry survey: https://www.tomshardware.com/tech-industry/semiconductors/the-state-of-abf-substrates-in-data-center-silicon-in-2026-solving-the-supply-crunch-and-material-wall-beneath-every-ai-accelerator — accessed 2026-09-17.
- HBM vendor qualification news (secondary): Silicon Analysts weekly notes — **Likely**/time-stamped.

**Unknown:** Official public split of Rubin HBM4 supply among SK hynix / Samsung / Micron (contractual; rarely disclosed precisely).
