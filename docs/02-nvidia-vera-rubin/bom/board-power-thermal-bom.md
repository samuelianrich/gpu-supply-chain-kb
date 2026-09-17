# Board / power / thermal BOM (tray and rack)

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |
|------|----------------|---------------------|----------|----------|-------|
| Superchip host board / midplane | Unknown | ODM PCB partners | Unknown | — | PCIe Gen6 midplane called out in Tech Blog graphics |
| GPU/CPU VRMs / power stages | Unknown | Infineon, TI, Monolithic Power, Vicor, etc. (**Speculative**) | Speculative | Industry AI-server pattern | Currents rise with Rubin TDP (**Unknown** official TDP) |
| Bulk capacitors / magnetics | Unknown | various | Unknown | — | |
| Cold plates | Unknown | Auras, CoolIT, Boyd, ODM (**Likely**) | Speculative | — | |
| Universal quick-disconnects | Unknown | CPC, Parker, etc. (**Speculative**) | Speculative | Tech Blog mentions universal QDs | |
| TIM / gap pads | Unknown | various | Unknown | — | |
| Cable-free tray connectors / blind-mate | Unknown | Amphenol, Molex, TE (**Speculative**) | Speculative | Tech Blog modular tray | |
| Rack-level energy buffer / caps | Unknown | — | Confirmed concept | Tech Blog (~6× buffering vs Blackwell Ultra claim) | Part numbers **Unknown** |
| Leak detection / sensors | Unknown | — | Confirmed Mission Control feature class | Tech Blog | |

**Unknown:** Official NVL72 rack power (kW), coolant flow rates, and qualified VRM BOM — typically ODM confidential or partner SKU-specific.
