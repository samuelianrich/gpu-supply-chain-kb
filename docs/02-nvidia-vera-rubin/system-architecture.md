# Vera Rubin — system architecture (rack-scale)

## Architectural thesis

Extreme co-design: GPUs, CPUs, scale-up (NVLink), scale-out (Ethernet/IB), DPUs, power, and cooling treated as one system. Data center / rack—not a single PCIe card—is the unit of compute.

(**Confirmed**; NVIDIA Technical Blog.)

## Superchip → tray → rack → POD

```text
Vera Rubin Superchip
  = 2× Rubin GPU + 1× Vera CPU (NVLink-C2C coherent)
        ↓
NVL72 Compute Tray
  = 2× Superchips + ConnectX-9 + BlueField-4 + liquid cooling
        ↓
NVL72 Rack
  = many compute trays + NVLink 6 switch trays
    → 72 GPUs + 36 CPUs all-to-all NVLink domain
        ↓
DGX SuperPOD / AI factory
  = multiple NVL72 + Spectrum-X scale-out + storage + Mission Control
```

(**Confirmed** structure in Technical Blog sections 3–4.)

## Scale-up fabric

- **NVLink 6:** 3.6 TB/s bidirectional per GPU; all-to-all across 72 GPUs; SHARP in-network compute on switch trays (**Confirmed**).
- Switch tray aggregates multiple NVLink 6 switch chips; rack NVLink domain bandwidth cited at **260 TB/s** class in product tables (**Confirmed** product page / datasheet figures).

## Scale-out

- **ConnectX-9** endpoints (up to 1.6 Tb/s networking bandwidth per GPU in tray descriptions) (**Confirmed** Tech Blog).
- **Spectrum-6** / Spectrum-X Ethernet Photonics with co-packaged optics; alternatively **Quantum-X800** InfiniBand in SPX rack configurations (**Confirmed** Newsroom).

## Memory domains

| Domain | Technology | Role |
|--------|------------|------|
| GPU HBM | HBM4 | Weights, activations, KV hot path |
| CPU DRAM | LPDDR5X SOCAMM | Orchestration, capacity, KV offload |
| Coherent link | NVLink-C2C 1.8 TB/s | Unified address space narrative |
| Pod storage | BlueField-4 STX / ICMS | Shared KV / context memory tier |

(**Confirmed** Tech Blog / Newsroom.)

## Power & cooling (system-level)

- Warm-water single-phase direct liquid cooling lineage from Blackwell; 45°C supply temperature discussed (**Confirmed** Tech Blog narrative).
- Rack-level power smoothing / energy buffering vs Blackwell Ultra (**Confirmed** as NVIDIA claims; quantitative “6x buffering” is NVIDIA statement — accept as **Confirmed** claim, independent measurement **Unknown**).
- DSX / Mission Control software for power domains (**Confirmed**).

## Separation reminder for BOM work

| Layer | Examples | BOM file |
|-------|----------|----------|
| Chip / package | Rubin GPU package, Vera CPU, HBM4 | logic / memory / package BOMs |
| Board / tray | Superchip board, VRMs, cold plates, CX9, BF4 | board-power-thermal |
| Rack / POD | Switch trays, CDUs, busbars, Spectrum racks | system-bom |

## Citations

- NVIDIA Technical Blog (architecture deep dive): https://developer.nvidia.com/blog/inside-the-nvidia-rubin-platform-six-new-chips-one-ai-supercomputer/ — accessed 2026-09-17.
- NVIDIA Newsroom (rack SKUs): https://nvidianews.nvidia.com/news/nvidia-vera-rubin-platform — accessed 2026-09-17.
