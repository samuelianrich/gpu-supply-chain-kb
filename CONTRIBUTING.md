# Contributing to this knowledge base

## Scope

Add or correct facts about semiconductor materials, wafer/fab/packaging/test flows, and NVIDIA Vera Rubin (or related AI GPU) supply-chain actors. Do not invent quantities. Prefer amending Evidence tags over deleting uncertainty.

## Adding or editing a claim

1. **Write the claim** in plain language.
2. **Attach an Evidence tag:** `Confirmed` | `Likely` | `Estimated` | `Speculative` | `Unknown`.
3. **Cite:** URL + publisher + date accessed (use `2026-09-17` format for access dates in this draft era) or publication date.
4. **If Unknown:** state what primary document, earnings call, or datasheet would confirm it.
5. **Add the URL** to `docs/03-sources/bibliography.md` if new.
6. **Raise open questions** in `docs/03-sources/open-questions.md` when a tracker signal is missing.

### Citation inline pattern

```markdown
Rubin GPUs ship with up to 288 GB HBM4 per GPU
(**Confirmed**; NVIDIA Technical Blog / product specs;
[NVIDIA Developer Blog](https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/),
accessed 2026-09-17).
```

### BOM table columns (required)

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |

Qty may be `Unknown` or `N/A`. Supplier candidates are not endorsements.

## Source preference order

1. Company IR, newsroom, official product/datasheet pages (NVIDIA, TSMC, SK hynix, Samsung, Micron, ASML, Ajinomoto, etc.)
2. SEMI, USGS Mineral Commodity Summaries, OECD value-chain reports
3. Reputable industry press / technical archives (IEEE Spectrum, AnandTech/Tom’s archives, SemiAnalysis-class analysis) — label carefully
4. DigiTimes / single-outlet Taiwanese trade press — treat as **Likely** or **Speculative** unless corroborated
5. Forums, leaks, anonymous social posts — **Speculative** only, or omit

## Confidence hygiene

- Never invent numbers (wafer starts, CoWoS WPM, die sizes, yields, $BOM).
- Separate **system-level** (rack, NVLink/NVSwitch, power, cooling) from **chip-level** (logic die, HBM, package).
- Foundry vs IDM vs OSAT roles must stay explicit.
- Geopolitics notes belong in “tracker signals,” not as causal certainty.

## What not to do

- Do not clone external git repos into this tree for the KB draft workflow described in the project brief.
- Do not push this tree to GitHub from the box as part of the draft task.
- Do not paste copyrighted textbooks verbatim; summarize process steps and cite.
