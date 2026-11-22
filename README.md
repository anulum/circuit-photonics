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

Circuit Photonics is being built as the conditional specialist repository for integrated silicon and silicon-nitride photonic circuits — executing `gdsfactory` waveguide layout and bend-curvature design-rule checks, separate-process `Meep` finite-difference time-domain verification, coupled 3D thermo-optic crosstalk sign-off and `sax` statistical wavelength/phase corner sweeps — completely deterministically without requiring AI. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed photonic layout builder, FDTD verification runner, S-matrix corner analyser or qualified record schema.

Circuit Photonics is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- a waveguide layout generator, FDTD runner or photonic circuit corner analyser;
- a registered runtime record schema;
- any migrated optical module or photonic mask layout.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Photonic view | Parametric `gdsfactory` waveguide, grating/edge-coupler, Mach-Zehnder, microring and photodetector layout, layer map, minimum bend-radius/gap rules and port coordinates |
| Photonic result | 3D `Meep` FDTD transmission/reflection spectra, dispersion, insertion-loss and thermo-optic phase-shift matrices, coupled thermal crosstalk margins and `sax` circuit-level wavelength/fabrication-variation corner bounds |

**Static imports:** only Circuit Core and Circuit Technology.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Core and Circuit Technology | entity references, design views, operation profiles, system budgets and technology profiles |
| Circuit Assembly | fibre-array, edge/grating coupler and package alignment views |
| Circuit Fields | 3D electro-thermal hotspot and heater crosstalk results |
| Circuit Flow and Circuit Learning | design-step learning records and grader bundle specifications |

**Capability registration and handoffs:** Registers under the specialist tool-profile manifest with Circuit Core, feeds photonic views and electro-optic S-matrix results to Circuit Physical, Circuit Assembly, Circuit Mixed-Signal and Circuit Acceptance, and receives generic photonic layer and FDTD modules split from SC-NeuroCore.

**Explicit non-claims and operating boundaries:**
- Every photonic layout, FDTD and S-matrix corner step completes deterministically without machine learning.
- Neural inverse-design geometry proposals are never accepted directly: every candidate geometry must pass separate-process `Meep` (`GPL-2.0`) 3D FDTD simulation, `gdsfactory` minimum-bend/width curvature DRC, 3D thermo-optic crosstalk checks and `sax` (`Apache-2.0`) statistical phase/wavelength corner sweeps.
- `Meep` (`GPL-2.0`) executes strictly as a separate child process over file boundaries.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
