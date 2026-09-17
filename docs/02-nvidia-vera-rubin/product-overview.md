# NVIDIA Vera Rubin — product overview

## What it is

**Vera Rubin** is NVIDIA’s rack-scale AI platform succeeding Grace Blackwell-era systems. It co-designs multiple chips so the **rack** (and POD) is the unit of compute.

(**Confirmed**; NVIDIA Newsroom, 2026-03-16; NVIDIA Technical Blog, 2026-01-05, updated 2026-03-16.)

### Naming

| Name | Role |
|------|------|
| **Vera** | Custom Arm-compatible CPU (Olympus cores); successor trajectory to Grace |
| **Rubin** | GPU / accelerator with HBM4 and Transformer Engine |
| **Vera Rubin platform** | Full chip + rack + networking + storage + software stack |
| **NVL72** | Flagship rack integrating 72 Rubin GPUs + 36 Vera CPUs |

## Publicly announced chips (platform)

NVIDIA states the platform brings together (**Confirmed**; Newsroom 2026-03-16):

1. NVIDIA **Vera** CPU  
2. NVIDIA **Rubin** GPU  
3. NVIDIA **NVLink 6** Switch  
4. NVIDIA **ConnectX-9** SuperNIC  
5. NVIDIA **BlueField-4** DPU  
6. NVIDIA **Spectrum-6** Ethernet switch  
7. Newly integrated **NVIDIA Groq 3 LPU** (seventh chip as of GTC 2026 update)

Technical Blog initially framed “six new chips”; Newsroom/GTC update adds Groq 3 (**Confirmed**).

## Rack / system SKUs (public)

| SKU / rack | Public content | Evidence |
|------------|----------------|----------|
| **Vera Rubin NVL72** | 72 Rubin GPUs + 36 Vera CPUs; NVLink 6; ConnectX-9; BlueField-4; claims vs Blackwell on MoE training GPU count and inference efficiency | **Confirmed** (Newsroom) |
| **Vera CPU Rack** | 256 Vera CPUs; liquid-cooled MGX; agentic/RL environments | **Confirmed** (Newsroom) |
| **Groq 3 LPX Rack** | 256 LPU processors; large on-chip SRAM / scale-up bandwidth claims; H2 availability with platform | **Confirmed** (Newsroom) |
| **BlueField-4 STX Storage Rack** | AI-native KV-cache / context memory storage tier | **Confirmed** (Newsroom) |
| **Spectrum-6 SPX Ethernet Rack** | Scale-out; configurable Spectrum-X or Quantum-X800 InfiniBand | **Confirmed** (Newsroom) |

Partner availability: products from partners starting **second half of 2026** (**Confirmed**; Newsroom). Clouds named: AWS, Google Cloud, Azure, OCI, plus NCPs (CoreWeave, Crusoe, Lambda, Nebius, Nscale, Together AI) (**Confirmed**).

## Key published GPU / CPU figures (selected)

From NVIDIA Technical Blog / product tables (**Confirmed** unless noted):

| Item | Value | Evidence |
|------|-------|----------|
| Rubin transistors | 336B (full chip) | **Confirmed** (Tech Blog table vs Blackwell 208B) |
| Rubin compute dies | 2 | **Confirmed** |
| Rubin NVFP4 inference | 50 PFLOPS | **Confirmed** |
| Rubin NVFP4 training | 35 PFLOPS | **Confirmed** |
| HBM4 capacity / BW per GPU | up to 288 GB / 22 TB/s | **Confirmed** |
| NVLink 6 per GPU | 3.6 TB/s bidirectional | **Confirmed** |
| Vera cores / threads | 88 Olympus / 176 spatial MT | **Confirmed** |
| Vera memory | up to 1.5 TB LPDDR5X @ up to 1.2 TB/s | **Confirmed** |
| NVLink-C2C | 1.8 TB/s | **Confirmed** |
| NVL72 GPU+CPU count | 72 + 36 | **Confirmed** |

## Known vs inferred (honesty box)

| Topic | Status |
|-------|--------|
| Platform chip list, NVL72 composition, HBM4, NVLink 6 bandwidths | **Confirmed** (NVIDIA primary) |
| TSMC process node (e.g., N3 / N3P) for Rubin | **Likely** in industry press; **not** consistently printed on NVIDIA newsroom pages reviewed — treat as non-Confirmed until NVIDIA/TSMC primary line |
| CoWoS-L as packaging vehicle | **Likely** (press / prior Blackwell path); **Unknown** as NVIDIA one-liner on product page |
| Exact HBM stack count (often “8”) | **Likely** secondary; reconcile with “Total NVIDIA + HBM4 Chips” table footnotes on product page |
| Die size mm² | **Unknown** publicly in sources reviewed |
| Unit BOM $ cost | **Unknown** / **Estimated** only in analyst notes |

## Citations

- https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — NVIDIA Newsroom, 2026-03-16, accessed 2026-09-17.
- https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — NVIDIA Technical Blog, 2026-01-05 (updated 2026-03-16), accessed 2026-09-17.
- https://www.nvidia.com/en-sg/data-center/vera-rubin-nvl72/ — product tables, accessed 2026-09-17.
