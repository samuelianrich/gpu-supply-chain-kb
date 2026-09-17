# 07 — Equipment, materials, and specialty gases (cross-cutting)

## What happens

Every prior stage depends on a **tool + materials** industrial base. For a tracker, this layer explains *why* capacity cannot spike quickly: tools have long lead times; chemistries are qualified per process recipe; gases need purity and logistics.

## Equipment (selected chokepoints)

| Domain | Chokepoint | Evidence posture |
|--------|------------|------------------|
| Lithography | ASML EUV scanners; Zeiss SMT optics | Sole-source / single-facility optics risk discussed widely (**Confirmed** ASML EUV monopoly in practice; Zeiss dependency **Likely** high) |
| Deposition / etch / CMP | Applied Materials, Lam, TEL, ASM | Oligopolies by segment (**Likely**) |
| Metrology | KLA-centric inspection | High share (**Estimated**) |
| Packaging bonders | ASMPT, BESI, etc. | Advanced packaging ramp sensitive (**Likely**) |
| Wafer fab facilities | Cleanroom contractors, ultrapure water, abatement | CapEx multi-year |

## Materials

| Material | Use | Notes |
|----------|-----|-------|
| Photoresists | Lithography | Japan-centric suppliers (JSR, TOK, Shin-Etsu, Fujifilm, Sumitomo) (**Likely**) |
| Photo masks / blanks | Pattern masters | Blanks: Shin-Etsu and others (**Likely**) |
| CMP slurries / pads | Planarization | Specialty chem |
| Precursor gases / liquids | ALD/CVD | Qualified per node |
| ABF | Substrates | Ajinomoto (**Confirmed** product role via IR) |
| Solder / underfill | Packaging | Multiple |

## Specialty gases

Examples used across FEOL/BEOL (illustrative, not a full BOM):

- Ultra-high-purity N₂, Ar, He
- H₂, O₂, NF₃, CF₄, C₄F₈, Cl₂, HBr, WF₆, etc. (recipe-specific)
- Bulk + cylinder logistics; on-site generation for some N₂

Regional gas majors (Air Liquide, Linde, Air Products, regional players) — **Likely** suppliers; fab contracts rarely public.

## Yield / risk notes

- A single resist plant outage can ripple to advanced nodes (historical Japan earthquake / plant event narratives — treat specific %-impact claims as **Estimated** unless primary).
- Helium supply shocks affect some tools/processes (**Likely** intermittent tracker item).
- Export controls on tools are as important as controls on chips.

## How this feeds a modern AI GPU

AI GPU ramps are simultaneously:

1. Wafer-start limited (EUV + foundry tools),
2. Package limited (CoWoS tools + HBM),
3. Materials limited (resist, ABF, gases),
4. System limited (power/cooling/ODM).

Equipment/materials are the ** CapEx calendar** behind those limits.

## Tracker signals

| Signal | Source type |
|--------|-------------|
| ASML shipment / backlog commentary | Primary IR |
| WFE (wafer fab equipment) spend forecasts | SEMI / vendor |
| Resist / specialty chem force majeure | Producer notices |
| Gas ASPs / helium | Industrial gas IR |
| TSMC / Samsung / Intel CapEx guides | Primary IR |

## Evidence & citations

- OECD (2025) value-chain dependencies (equipment & materials concentration): https://www.oecd.org/content/dam/oecd/en/publications/reports/2025/06/mapping-the-semiconductor-value-chain_5ba52971/4154cdbf-en.pdf — accessed 2026-09-17.
- Ajinomoto ABF materials positioning: company electronic materials briefing PDF — accessed 2026-09-17 (see bibliography).
- Semiconductor bottleneck atlases (secondary): useful checklists; validate before quantifying.

**Unknown:** Full qualified materials list for TSMC N3 HPC + CoWoS-L used on Rubin (proprietary).
