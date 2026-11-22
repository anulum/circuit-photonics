<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-PHOTONICS — repository foundation
-->

# Circuit Photonics

Circuit Photonics is being built as the conditional specialist repository for integrated silicon and silicon-nitride photonic circuits — executing `gdsfactory` waveguide layout and bend-curvature design-rule checks, separate-process `Meep` finite-difference time-domain verification, coupled 3D thermo-optic crosstalk sign-off and `sax` statistical wavelength/phase corner sweeps — completely deterministically without requiring AI. Its current executable surface is repository validation tooling. It has no installed photonic layout builder, FDTD verification runner, S-matrix corner analyser or qualified record schema.

Read [Architecture](ARCHITECTURE.md), [validation tooling](validation-tooling.md), [data boundaries](THREAT_MODEL.md) and the [repository boundary decision](adr/0001-repository-boundary.md).
