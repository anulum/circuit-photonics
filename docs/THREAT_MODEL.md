<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-PHOTONICS — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- photonic netlists, parametric cell parameters and inverse-design polygons;
- foundry dispersion tables and thermal coupling maps.

They grant no authority to:
- sign off an inverse-designed polygon without full FDTD, curvature-DRC and statistical corner verification;
- link `GPL` `Meep` libraries in-process;
- release mask files or spend.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Inverse-designed photonic geometries failing fab curvature rules, dispersion or thermo-optic crosstalk | Every candidate geometry must pass `gdsfactory` bend/width DRC, separate-process 3D `Meep` FDTD verification, 3D thermal crosstalk coupling from Circuit Fields and `sax` statistical corner sweeps |
| Copyleft FDTD solver linkage | `Meep` (`GPL-2.0`) executes strictly in a separate process over file boundaries |

## Residuals named, not removed

- **Sidewall roughness.** Waveguide scattering loss depends on foundry etch-roughness calibration anchored post-silicon.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
