# TSMC process and packaging role (Vera Rubin)

## Confirmed (primary)

| Claim | Evidence | Citation |
|-------|----------|----------|
| NVIDIA relies on third parties to manufacture, assemble, package, and test products | Risk factor language in Vera Rubin release | NVIDIA Newsroom 2026-03-16 |
| Rubin GPU uses **HBM4** | Product/tech materials | NVIDIA Tech Blog / NVL72 pages |
| Multi-die GPU (2 compute dies in comparison tables) | Tech Blog Blackwell vs Rubin table | NVIDIA Tech Blog |
| Advanced packaging is required for HBM+logic AI GPUs generally | Industry + NVIDIA packaging dependence | See lifecycle packaging docs |

NVIDIA’s public Vera Rubin pages emphasize **architecture and performance**, not a marketing line like “TSMC N3P + CoWoS-L” on every consumer-facing URL reviewed for this draft.

## Likely (industry press / continuity with Blackwell)

| Claim | Why “Likely” | Caution |
|-------|--------------|---------|
| Logic foundry is **TSMC** | Longstanding NVIDIA HPC pattern; Huang commentary on Rubin tapeouts at TSMC reported in trade press | Prefer NVIDIA IR or TSMC customer quotes |
| Process node **N3 / N3P class** | Multiple 2025–2026 trade articles cite N3P + trial production | Not elevated to Confirmed here |
| Packaging **CoWoS-L** | Continuity from Blackwell multi-die + HBM; analyst/press consensus | Await TSMC symposium slide / NVIDIA explicit naming |
| Taiwan AP site concentration | TSMC CoWoS capacity geography | Site-level lists often secondary |

Example secondary: TechPowerUp summary of Huang Taiwan comments on Rubin trial production / N3P / CoWoS-L — treat as **Likely/Speculative** pending primary transcript (**Citation:** https://www.techpowerup.com/340207/nvidia-rubin-platform-enters-trial-production-at-tsmc-ceo-jensen-huang-confirms — accessed 2026-09-17).

## Estimated (capacity narrative — tracker only)

Secondary trackers in 2026 describe CoWoS monthly capacity rising toward ~120–130k WPM-class targets with long booking windows (**Estimated**; Silicon Analysts / similar). NVIDIA share of CoWoS often cited around majority percentage (**Estimated**). Use only as directional tracker signals, never as accounting facts.

## Speculative

- Exact mask set counts, wafer starts per NVL72, or die mm².
- Non-TSMC backup foundry for Rubin compute dies in volume.
- SoIC use on Rubin compute stack.

## What would move claims to Confirmed

1. NVIDIA investor presentation slide naming process node + package type for Rubin GPU and Vera CPU separately.  
2. TSMC Technology Symposium or earnings Q&A explicitly tying CoWoS-L volume to Rubin.  
3. SEC filing detail (rare at this granularity).

## Implications for supply-chain tracker

Even with Unknown node strings, **binding constraints** remain:

1. Leading-edge wafer capacity  
2. CoWoS / advanced packaging slots  
3. HBM4 availability & qualification  
4. ABF substrates for large packages  
5. ODM rack + liquid-cooling throughput  

## Citations

- NVIDIA Newsroom: https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17.
- NVIDIA Tech Blog: https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17.
- Secondary TSMC/CoWoS capacity: https://siliconanalysts.com/analysis/foundry-allocation-status-q1-2026 — accessed 2026-09-17 (**Estimated** figures).
