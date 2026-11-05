---
layout: default
title: What v1 Is Not
nav_order: 17
description: "Intake v1's explicit boundaries: no retopology, no quad topology, no UV repair, no deformation readiness, no glTF processing, and no AI inside Intake itself."
---

# What v1 Is Not
{: .no_toc }

This page ships inside the package as well as here. Intake v1's boundaries, stated before you buy rather than after:

- **Not a retopologiser.** Intake decimates to a budget. It does not retopologise, does not produce quad topology or clean edge flow, and its output is **not deformation-ready** — the report card for every reduced mesh says so, in those words.
- **Not for characters.** Intake refines **static props and environment pieces**. Skinned, rigged or animated meshes are detected and routed to **Needs human pass** — never reduced, never given an LOD chain, never turned into a prefab.
- **Not a UV tool.** Source UVs are preserved and checked, **not repaired or rebuilt**.
- **Not a glTF pipeline.** Version 1 does not import or process glTF/GLB. A .glb/.gltf file is detected, listed as **Not supported in v1**, and answered with the FBX instruction only. See [Formats]({{ site.baseurl }}/docs/formats/).
- **Not "AI-powered."** Intake uses **no AI**. It refines the output of AI model generators — deterministically, locally, on files.
- **Not a perfect converter.** Converted materials are a faithful mapping to your pipeline's standard lit shader, not a claim of perfect reproduction; channels that cannot be mapped are named **Not converted** on the card.
- **Not instant on dense meshes.** Decimation of a very dense model takes minutes, not seconds — roughly four minutes for the Messy Crate's ~184,000 triangles.
- **Not a runtime.** Editor-only tooling; it adds nothing to your player build, and the output — ordinary meshes, materials, textures and prefabs — is your project's own data outright.
