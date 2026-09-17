# Memory / HBM BOM

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |
|------|----------------|---------------------|----------|----------|-------|
| HBM4 capacity per Rubin GPU | up to 288 GB | SK hynix, Samsung, Micron | Confirmed capacity | Tech Blog / NVL72 tables | Vendor split **Unknown** |
| HBM4 bandwidth per GPU | up to 22 TB/s | same | Confirmed | Tech Blog | |
| HBM4 stacks per GPU | Unknown (often reported as 8) | same | Likely | Secondary architecture writeups | Confirm via datasheet / teardown |
| HBM4 base/logic die | 1 per stack | Memory IDM | Likely | JEDEC HBM architecture | Custom base die rumors = **Speculative** |
| NVL72 aggregate HBM4 | 20.7 TB | — | Confirmed | NVL72 product tables | 72 × 288 GB |
| Vera LPDDR5X | up to 1.5 TB per CPU | DRAM vendors (Micron, Samsung, SK hynix) (**Likely**) | Confirmed capacity | Tech Blog | SOCAMM form factor |
| Vera LPDDR5X bandwidth | up to 1.2 TB/s | same | Confirmed | Tech Blog | |

### Tracker notes

HBM4 qualification status is time-varying; secondary trackers report multi-vendor qualification activity (**Likely**/Estimated). Do not treat share % as Confirmed without vendor IR or NVIDIA disclosure.

### Citations

- https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17
- https://www.nvidia.com/en-sg/data-center/vera-rubin-nvl72/ — accessed 2026-09-17
