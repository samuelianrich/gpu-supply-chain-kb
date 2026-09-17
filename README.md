# GPU Supply-Chain Knowledge Base

Living tracker knowledge base for semiconductor supply chains that feed modern AI GPUs, with a focused scaffold for **NVIDIA Vera Rubin** systems built with TSMC foundry/packaging capacity.

**Status:** First substantive draft (box filesystem only). Not a git repo push target.  
**Access date for citations in this draft:** 2026-09-17 (America/Phoenix local box clock).

---

## Purpose

1. Map the **general GPU production lifecycle** from quartz/sand → metallurgical/electronic-grade silicon → wafers → front-end fab → advanced packaging → HBM/substrate → assembly/test.
2. Scaffold a **product lifecycle + bill of materials (BOM)** for NVIDIA’s Vera Rubin platform (Vera CPU + Rubin GPU + rack-scale SKUs), separating confirmed public facts from industry inference.
3. Give a supply-chain **tracker** a durable place to hang lead-time, capacity, geopolitics, and open questions—without inventing numbers.

---

## How to read Evidence tags

Every non-trivial factual claim in this KB should carry:

| Tag | Meaning |
|-----|---------|
| **Confirmed** | Stated by a primary source (company IR/newsroom, official product page, SEMI/USGS/OECD, peer-reviewed or textbook process description attributed to a named reputable source). |
| **Likely** | Consistent across multiple reputable secondary sources or strongly implied by primary context, but not a direct one-line confirmation. |
| **Estimated** | Quantitative or qualitative estimate from analysts/press; treat as directional only. |
| **Speculative** | Rumor, single-source leak, or extrapolation; do not use for decisions without follow-up. |
| **Unknown** | Not established in public sources reviewed for this draft; note what would confirm it. |

Each tagged claim also needs a **citation**: URL + publisher + date accessed (or source publication date). Prefer primary sources. See [CONTRIBUTING.md](CONTRIBUTING.md) and [docs/03-sources/bibliography.md](docs/03-sources/bibliography.md).

---

## Reading order

1. **Lifecycle first** — start with the end-to-end map, then sand-to-chip stages:
   - [docs/00-overview/supply-chain-map.md](docs/00-overview/supply-chain-map.md)
   - [docs/01-lifecycle-sand-to-chip/](docs/01-lifecycle-sand-to-chip/) (01 → 07)
2. **Then Vera Rubin** — product overview → architecture → TSMC process/packaging → BOM → actors:
   - [docs/02-nvidia-vera-rubin/](docs/02-nvidia-vera-rubin/)
3. **Sources & gaps** — bibliography and open questions:
   - [docs/03-sources/bibliography.md](docs/03-sources/bibliography.md)
   - [docs/03-sources/open-questions.md](docs/03-sources/open-questions.md)

---

## Document map

```
gpu-supply-chain-kb/
  README.md
  CONTRIBUTING.md
  docs/
    00-overview/
      supply-chain-map.md
    01-lifecycle-sand-to-chip/
      01-quartz-and-polysilicon.md
      02-ingot-wafer.md
      03-front-end-fab.md
      04-advanced-packaging.md
      05-substrate-hbm-interposer.md
      06-assembly-test.md
      07-equipment-materials-gases.md
    02-nvidia-vera-rubin/
      product-overview.md
      system-architecture.md
      tsmc-process-and-packaging.md
      bom/
        README.md
        system-bom.md
        logic-die-bom.md
        memory-hbm-bom.md
        package-substrate-bom.md
        board-power-thermal-bom.md
      supply-chain-actors.md
    03-sources/
      bibliography.md
      open-questions.md
```

---

## Living tracker note

This is a **living** knowledge base. Process nodes, CoWoS capacity, HBM qualifications, and Vera Rubin BOM details will change as NVIDIA, TSMC, memory vendors, and substrate/OSAT suppliers publish updates. Prefer amending Evidence tags and citations over rewriting narrative from memory. When a claim moves from Speculative → Confirmed, keep the old citation trail in Notes where useful.
