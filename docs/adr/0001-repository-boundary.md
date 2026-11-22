<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-PHOTONICS — repository foundation
-->

# Decision: isolate silicon-photonic layout, FDTD verification and S-matrix corners in Circuit Photonics

## Context

Optical neuromorphic and interconnect blocks obey curvilinear waveguide rules, wavelength dispersion and thermo-optic phase sensitivity absent from Manhattan electronic place-and-route flows.

## Decision

**What Circuit Photonics owns:**
- photonic view;
- photonic result;

**What it imports:** only Circuit Core and Circuit Technology.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| 3D thermal and RF solving | Circuit Fields |
| electro-optic mixed-signal co-simulation | Circuit Mixed-Signal |
| full-chip GDSII merge and DRC | Circuit Physical |
| fibre-attach and package assembly | Circuit Assembly |
| tapeout sign-off | Circuit Acceptance |

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- Circuit Photonics stays optional for purely electronic chips while giving electro-optic designs deterministic `gdsfactory`, `Meep` and `sax` verification;
- electro-optic interface co-simulation connects cleanly through Circuit Mixed-Signal.
