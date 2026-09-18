# From Sand to GPU — video series

Narrated 16:9 explainers (~3–5 min) derived from `docs/01-lifecycle-sand-to-chip/` and related knowledge-base pages.

## Format
- Generated educational slides + TTS narration + ffmpeg assembly
- Claims follow the same Evidence discipline as the markdown KB (Confirmed / Likely / Estimated / Speculative / Unknown)
- Slides must not invent dashboard metrics; use conceptual labels only

## Episodes
| Episode | Title | Source doc | Status |
|---------|-------|------------|--------|
| 01 | From Quartz to Polysilicon | `docs/01-lifecycle-sand-to-chip/01-quartz-and-polysilicon.md` | Pilot MP4 in `ep01/out/` |
| 02 | From Ingot to Wafer | `docs/01-lifecycle-sand-to-chip/02-ingot-wafer.md` | Pilot MP4 in `ep02/out/` |
| 03 | Inside the Front-End Fab | `docs/01-lifecycle-sand-to-chip/03-front-end-fab.md` | Pilot MP4 in `ep03/out/` |

## Episode layout
Each episode follows this structure:
- `epNN/scripts/narration.txt` — teleprompter / TTS script
- `epNN/scripts/slides.json` — slide plan
- `epNN/slides/` — 1920×1080 frames
- `epNN/audio/` — narration MP3 + VTT
- `epNN/out/epNN-title.mp4` — assembled pilot

## Large media
The assembled MP4 files are committed in each episode's `out/` directory (~13–15MB each).
