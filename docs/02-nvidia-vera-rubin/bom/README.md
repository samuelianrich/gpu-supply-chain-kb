# Vera Rubin BOM scaffold

Bill-of-materials tables for the NVIDIA Vera Rubin platform. **Separate system-level from chip-level.**

| File | Scope |
|------|--------|
| [system-bom.md](system-bom.md) | Rack / POD: GPUs, CPUs, switches, NICs, DPUs, cooling, power shelves |
| [logic-die-bom.md](logic-die-bom.md) | Logic silicon inside packages (Rubin compute, Vera, NVLink switch, etc.) |
| [memory-hbm-bom.md](memory-hbm-bom.md) | HBM4 stacks and related |
| [package-substrate-bom.md](package-substrate-bom.md) | CoWoS-class package, interposer/bridges, ABF substrate |
| [board-power-thermal-bom.md](board-power-thermal-bom.md) | Tray/board VRMs, cold plates, connectors, TIM |

## Column convention

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |

- **Qty:** use `Unknown` when not public; do not invent.
- **Supplier candidates:** not purchase recommendations; qualification may lag.
- **Evidence:** Confirmed | Likely | Estimated | Speculative | Unknown.

## Honesty rules

NVIDIA publishes platform composition (e.g., 72 GPUs / 36 CPUs in NVL72) but rarely publishes full commercial BOMs, die suppliers by percentage, or substrate vendor awards. Empty cells and **Unknown** rows are success criteria for this draft.
