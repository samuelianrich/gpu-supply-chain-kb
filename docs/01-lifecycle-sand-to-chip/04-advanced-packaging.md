# 04 — Advanced packaging (CoWoS-class and related)

## What happens

After front-end, AI GPU dies are not finished products. They are integrated in **2.5D / 3D advanced packaging**:

1. Prepare known-good logic dies and HBM stacks.
2. Attach dies to an **interposer** or **RDL + local silicon bridges**.
3. Bond the assembly to an **organic package substrate** (often ABF-based FC-BGA).
4. Attach package to board / module (or ship as BGA component).

TSMC’s family brand for this HPC path is **CoWoS** (Chip-on-Wafer-on-Substrate):

| Variant | High-level idea | Typical use narrative |
|---------|-----------------|----------------------|
| **CoWoS-S** | Silicon interposer | Classic large interposer; reticle-size limits bite hard |
| **CoWoS-L** | Organic RDL with **local silicon interconnect (LSI) bridges** | Enables larger multi-reticle packages (Blackwell/Rubin narratives in press) |
| **CoWoS-R** | RDL-focused variant | Product-dependent |

(**Confirmed** that CoWoS is TSMC’s advanced packaging platform for integrating logic with HBM in AI/HPC; **Likely** that CoWoS-L is the growth path for multi-die NVIDIA GPUs per industry analysis—attach primary TSMC symposium slides when available.)

### SoIC-like concepts (high level)

**SoIC** (System-on-Integrated-Chips) refers to TSMC’s bonding approaches for finer-pitch 3D stacking (logic-on-logic or related). Treat SoIC as **adjacent** to CoWoS: some products may combine 3D stacking with 2.5D HBM integration. Exact use on Vera Rubin is **Unknown** without NVIDIA/TSMC primary confirmation.

## Key materials / inputs

- Logic KGD + HBM KGD
- Silicon interposer wafers *or* LSI bridge dies + RDL materials
- Microbumps / hybrid bonds
- Underfill / capillary materials
- Package substrate (see doc 05)
- Thermal interface materials (TIM) later at module level

## Typical suppliers / regions

| Role | Actors | Region notes |
|------|--------|--------------|
| Advanced packaging capacity | **TSMC** backend (AP sites in Taiwan: Longtan, Taichung, Zhunan, Chiayi, Tainan expansions reported) | Taiwan concentration (**Likely**/site names from industry press—verify with TSMC) |
| OSAT alternatives | Amkor, ASE, JCET, etc. | Growing advanced packaging, but NVIDIA HPC historically TSMC CoWoS-centric (**Likely**) |
| Equipment | Applied Materials, ASMPT, BESI, Disco, Kulicke & Soffa (segment-dependent) | Global |

TSMC and multiple industry sources described AI frontend **and** backend capacity as very tight into 2025–2026 (**Confirmed** as qualitative commentary when quoted from earnings; numeric WPM figures usually **Estimated**).

## Process equipment classes

- Chip-on-wafer bonders
- Wafer thinning / TSV reveal (for interposer flows)
- RDL patterning tools
- Flip-chip bonders
- Underfill dispensers / cure
- X-ray / scanning acoustic microscopy for voids
- Thermal compression bonding tools (for finer pitches)

## Yield / risk notes

- Large packages → thermo-mechanical stress, warpage, microbump yield.
- CoWoS-L trades giant interposer yield risk for bridge + RDL complexity (**Likely**; analyst cost/yield narratives).
- **Lead times** of 52–78 weeks for CoWoS slots appear repeatedly in 2026 secondary trackers (**Estimated**; useful as a signal, not a hard fact without TSMC primary).

## How this feeds a modern AI GPU

This is the step where a GPU becomes an **AI accelerator package**: multi-die logic + **8 HBM stacks** class memory (product-specific). Without CoWoS-class capacity, front-end wafers sit as unfinished inventory.

For Vera Rubin, NVIDIA publicly emphasizes HBM4 on the Rubin GPU and rack-scale integration; packaging technology brand/node details are handled in the Vera Rubin TSMC note.

## Tracker signals

| Signal | Why |
|--------|-----|
| TSMC CoWoS capacity commentary (earnings) | Binding constraint narrative |
| AP site equipment move-in | Leading indicator |
| NVIDIA % of CoWoS allocation | Competitive intensity (**Estimated** in press) |
| Package size / reticle multiplier rumors | Substrate & yield stress |
| OSAT CoWoS-like competitive offerings | Diversification |

## Evidence & citations

- Industry explainers on CoWoS as HBM+logic integration bottleneck (qualitative): Fusion Worldwide / similar 2026 analyses — use for framing; prefer TSMC earnings quotes for **Confirmed** tightness. Example: https://info.fusionww.com/blog/inside-the-ai-bottleneck-cowos-hbm-and-2-3nm-capacity-constraints-through-2027 — accessed 2026-09-17.
- Secondary capacity/lead-time trackers (Silicon Analysts et al.): treat WPM and 52–78 week lead times as **Estimated**. https://siliconanalysts.com/analysis/cowos-lead-times-ai-bottleneck-2026 — accessed 2026-09-17.
- NVIDIA reliance on third-party packaging (**Confirmed** risk factor language): https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17.

**Unknown:** Official TSMC public confirmation of CoWoS-L (vs S) as the Rubin production vehicle in a single primary slide—industry press asserts it (**Likely**), NVIDIA product pages emphasize performance not CoWoS SKU name.
