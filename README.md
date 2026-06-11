# GPR surface & bed picking survey

This repository hosts a small, browser-based survey used to evaluate how
consistently experts manually pick reflections in **UAV-borne ground-penetrating
radar (GPR)** radargrams of Alpine glaciers. Each participant traces two
horizons — the glacier **surface** and the **bed** — on a set of radargrams; the
spread between participants quantifies the picking contribution to the
ice-thickness uncertainty.

It is part of the **[MELT.AI](https://www.georesearch.ac.at/en/areas/research/research-projects/project-meltai/)**
project (UAV-borne GPR measurements of remaining glacier ice volume in the
Eastern Alps).

## Live survey

➡️ **https://anna7br.github.io/radargrams/**

The page opens with instructions; participants click **Start picking**, trace the
surface and bed on each radargram, **download** their results as a CSV, and
**upload** that file through a linked Google Form.

## How it works

The survey is fully **static** (no server): it runs entirely in the visitor's
browser. Picks are stored in the browser tab until the participant downloads them
as a VIA-style CSV (polyline vertices in image pixels), then returned via an
external upload form. Vertical pixel→thickness calibration is handled offline by
the analysis script using each radargram's sampling interval and a fixed export
sample height.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | Landing page with participant instructions and links |
| `bed_pick_annotator.html` | The browser picking tool (canvas annotator) |
| `images.js`, `images.json` | List of radargram image files loaded by the tool |
| `*.png` | The radargram images (rulers-off B-scans, 5 px per sample) |

## Data and reuse

The radargrams are research data from the MELT.AI project and are provided here
solely for the purpose of this picking study. They are **© GEORESEARCH** and are
**not** (yet) released for redistribution or other use without permission. Please
contact the author before reusing any material from this repository.

## Contact

**Anna Siebenbrunner** — GEORESEARCH & Technical University of Munich
<anna.siebenbrunner@georesearch.ac.at>
