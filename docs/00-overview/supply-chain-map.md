# End-to-end supply-chain map (sand → packaged AI GPU)

This map links lifecycle stages to the actors and bottlenecks that matter for a modern AI GPU (logic + HBM in CoWoS-class advanced packaging, then board/rack).

## Stage flow

```text
[1] Quartz / silica mining & HPQ
        ↓
[2] Metallurgical-grade Si → polysilicon (EG / solar grades)
        ↓
[3] Crystal growth (CZ ingot) → wafering (200mm / 300mm)
        ↓
[4] Front-end fab (FEOL + BEOL): deposition, etch, implant, CMP, litho (DUV/EUV)
        ↓  foundry (e.g. TSMC) or IDM
[5] Wafer sort / Known Good Die (KGD)
        ↓
[6] Advanced packaging: CoWoS-S / CoWoS-L / CoWoS-R (+ SoIC-like 3D concepts)
        ├─ silicon interposer or RDL + local Si bridges
        ├─ HBM stacks (SK hynix / Samsung / Micron)
        └─ organic / ABF package substrate
        ↓
[7] Final assembly & test (OSAT / foundry backend) → module / board
        ↓
[8] System integration: GPU tray, NVLink/NVSwitch, CPU, NIC/DPU, power, liquid cooling, rack
```

## Document links by stage

| Stage | Doc | Primary outputs |
|-------|-----|-----------------|
| Quartz → polysilicon | [01-quartz-and-polysilicon.md](../01-lifecycle-sand-to-chip/01-quartz-and-polysilicon.md) | EG polysilicon feedstock |
| Ingot → wafer | [02-ingot-wafer.md](../01-lifecycle-sand-to-chip/02-ingot-wafer.md) | 300mm polished wafers |
| Front-end fab | [03-front-end-fab.md](../01-lifecycle-sand-to-chip/03-front-end-fab.md) | Patterned logic / base dies |
| Advanced packaging | [04-advanced-packaging.md](../01-lifecycle-sand-to-chip/04-advanced-packaging.md) | Chip-on-wafer / multi-die package |
| Substrate + HBM + interposer | [05-substrate-hbm-interposer.md](../01-lifecycle-sand-to-chip/05-substrate-hbm-interposer.md) | ABF substrate, HBM, interposer/bridges |
| Assembly & test | [06-assembly-test.md](../01-lifecycle-sand-to-chip/06-assembly-test.md) | Tested packaged device |
| Equipment / materials / gases | [07-equipment-materials-gases.md](../01-lifecycle-sand-to-chip/07-equipment-materials-gases.md) | CapEx & process chemicals |
| Vera Rubin application | [../02-nvidia-vera-rubin/](../02-nvidia-vera-rubin/) | Platform BOM + actors |

## Critical chokepoints for AI GPUs (tracker view)

| Chokepoint | Why it gates GPUs | Typical Evidence posture |
|------------|-------------------|--------------------------|
| Leading-edge logic wafers (N3/N2 class) | Dies cannot exist without foundry starts | Capacity claims often **Estimated**; node for a named SKU needs **Confirmed** vendor statement |
| EUV lithography (ASML + Zeiss optics) | Sole-source scanners for finest layers | Equipment sole-source role **Confirmed** in industry literature; tool counts **Estimated** |
| CoWoS / advanced packaging | Logic + HBM cannot ship without backend slots | Demand/capacity narratives often **Estimated**; TSMC “tight capacity” commentary **Confirmed** when from earnings |
| HBM (HBM3E / HBM4) | Memory stacks are co-qualified with package | Vendor roadmap **Confirmed**; NVIDIA allocation shares **Estimated** |
| ABF / FC-BGA substrates | Large AI packages need high-layer-count substrates | Ajinomoto ABF role **Likely/Confirmed** via company IR; substrate maker mix **Estimated** |
| High-purity quartz crucibles | CZ crystal growth depends on HPQ | USGS HPQ demand notes **Confirmed** |

## How this feeds Vera Rubin

NVIDIA’s Vera Rubin platform is a **rack-scale** product: Rubin GPUs with HBM4, Vera CPUs with LPDDR5X, NVLink 6 switches, ConnectX-9, BlueField-4, Spectrum-6, plus optional Groq 3 LPU integration (**Confirmed**; NVIDIA Newsroom / Technical Blog, accessed 2026-09-17).

The sand-to-chip path below produces the **logic dies** and **memory stacks** that TSMC (and memory vendors) assemble into packages; board/rack partners then build NVL72-class systems. Process node and exact CoWoS flavor for Rubin are treated carefully in [tsmc-process-and-packaging.md](../02-nvidia-vera-rubin/tsmc-process-and-packaging.md)—NVIDIA publicly confirms HBM4 and packaging *dependence on third parties*, but does not always publish the foundry node string on every page.

## Evidence note

This overview is a navigation map. Stage docs carry per-claim Evidence tags and citations.
