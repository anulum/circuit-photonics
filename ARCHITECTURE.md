<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-PHOTONICS — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Photonics is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Waveguide layout and curvature DRC** generate photonic mask views and verify bend radii, waveguide widths, crossing angles and fibre-port pitches.
2. **Separate-process FDTD and thermo-optic coupling** run `Meep` electromagnetic sweeps combined with 3D thermal crosstalk maps from Circuit Fields.
3. **Circuit S-matrix corner sign-off** evaluates `sax` wavelength, waveguide-width/thickness and heater-phase corners for mixed-signal, physical and acceptance consumers.

## Ownership

**This project owns** the planned Circuit Photonics records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| 3D thermal and RF solving | Circuit Fields |
| electro-optic mixed-signal co-simulation | Circuit Mixed-Signal |
| full-chip GDSII merge and DRC | Circuit Physical |
| fibre-attach and package assembly | Circuit Assembly |
| tapeout sign-off | Circuit Acceptance |

## Interpretation

- **Grid resolution.** FDTD accuracy holds within its verified spatial-step convergence.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
