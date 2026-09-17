# Package / substrate / interposer BOM

| Item | Qty (if known) | Supplier candidates | Evidence | Citation | Notes |
|------|----------------|---------------------|----------|----------|-------|
| Advanced package (CoWoS-class) | 1 per GPU | TSMC CoWoS-L (**Likely**) | Likely | Industry press; NVIDIA does not always name CoWoS SKU on product pages | CoWoS-S vs L **Unknown** as NVIDIA one-liner |
| Silicon interposer | 0 or 1 | TSMC | Depends on CoWoS-S vs L | Packaging docs in this KB | CoWoS-L uses local bridges |
| Local silicon interconnect (LSI) bridges | Unknown | TSMC | Likely if CoWoS-L | Secondary packaging analyses | Count **Unknown** |
| Organic / ABF FC-BGA substrate | 1 per GPU package | Unimicron, Ibiden, Shinko, Nan Ya, SEMCO, AT&S | Likely vendor set | Tom’s Hardware 2026 ABF survey | Awarded vendor **Unknown** |
| ABF dielectric film | N/A (consumed by substrate maker) | Ajinomoto Fine-Techno | Confirmed product role | Ajinomoto IR PDF | Near-sole source narrative |
| Microbumps / C4 / solder balls | Unknown | materials cos. | Unknown | — | |
| Lid / heat spreader | Unknown | various | Unknown | — | |
| Underfill | Unknown | Namics, Henkel, etc. (**Speculative**) | Speculative | Industry | |

### Citations

- Ajinomoto electronic materials briefing: https://www.ajinomoto.co.jp/company/en/ir/event/business_briefing/main/011117/teaserItems1/01/linkList/03/link/20260630_presentation_E.pdf — accessed 2026-09-17
- Tom’s Hardware ABF 2026: https://www.tomshardware.com/tech-industry/semiconductors/the-state-of-abf-substrates-in-data-center-silicon-in-2026-solving-the-supply-crunch-and-material-wall-beneath-every-ai-accelerator — accessed 2026-09-17
