<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-PHOTONICS — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Photonic view | Parametric `gdsfactory` waveguide, grating/edge-coupler, Mach-Zehnder, microring and photodetector layout, layer map, minimum bend-radius/gap rules and port coordinates | Pinned design-view, technology-profile and fibre-array assembly-view digests with zero curvature or width violations |
| Photonic result | 3D `Meep` FDTD transmission/reflection spectra, dispersion, insertion-loss and thermo-optic phase-shift matrices, coupled thermal crosstalk margins and `sax` circuit-level wavelength/fabrication-variation corner bounds | Separate-process FDTD provenance, grid-resolution convergence check and coupled thermal inputs from Circuit Fields |

## Licence isolation

- **Permissive layout/S-matrix, separate-process FDTD.** `gdsfactory` and `sax` (`MIT` / `Apache-2.0`) run under permissive terms, while `Meep` (`GPL-2.0`) runs strictly as a separate child process over geometry and spectrum files.

## Planned record schemas

- `circuit_photonics.photonic_view.v1`
- `circuit_photonics.photonic_result.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
