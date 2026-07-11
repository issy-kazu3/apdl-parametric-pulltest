# PULLTEST — Parametric APDL Model for Resin–Busbar Pull Test
Fully scripted APDL pull-test model (no GUI)

## Overview
This repository contains a fully scripted APDL model for simulating a resin–busbar pull test.
The model is 100% parametric, including geometry, mesh, materials, and loading conditions.

Key features:

- Parametric geometry (busbar + resin + fine regions)

- Material library loading via MPREAD

- Automatic mesh sizing based on dimensions

- No GUI operations required

- Practical example of APDL-based automation

## Repository Structure
- docs/  
  Example output and reference documents

- material/  
  Material data files used by MPREAD

- src/  
  APDL script (PULLTEST.txt) and model-specific README

## Geometry
The model constructs the busbar and resin using multi-layered coordinate arrays:

- BUSTOP, BUS2ND, BUS3RD

- FINERESINTRI, FINERESIN

- TBUS, RESINTBUS, RESINCENTER

These arrays define all key points for PRISM and V-volume generation.

## Materials
Materials are loaded from external SI-unit libraries:

- RESIN (epoxy)

- Cu (busbar)

Si, Al, CuMo (optional regions)
