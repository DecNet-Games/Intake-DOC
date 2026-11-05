---
layout: default
title: FAQ
nav_order: 18
description: "Short answers: formats and glTF, what happens to characters, retopology, UVs, budgets, generators, runtimes, and what verification actually ran."
---

# FAQ
{: .no_toc }

## Does Intake import GLB files?

No. Version 1 does not import or process glTF/GLB. A .glb or .gltf file in the Inbox is **detected**, listed as **Not supported in v1**, and answered with one instruction: export the model as FBX from your generator and drop the FBX in the Inbox. See [Formats — FBX, OBJ and glTF]({{ site.baseurl }}/docs/formats/).

## Which generators does Intake work with?

Any of them. Intake processes **files, not services** — FBX and OBJ output from Meshy, Tripo, Rodin, Hunyuan, TRELLIS, a collaborator's export, or a hand-made model all take the identical path. No vendor account, no cloud call.

## Will Intake clean up my character model?

No — deliberately. Skinned, rigged or animated meshes are classified **Needs human pass**: no reduction, no LOD chain, no prefab. The card carries the detection evidence and the one next action. Intake refines static props and environment pieces.

## Is the output retopologised and ready to animate?

No. Output is **decimated**, not retopologised — no quad topology, no clean edge flow, not deformation-ready. Every reduced mesh's report card says so in those words.

## Does Intake fix broken UVs?

No. Source UVs are preserved and checked, **not repaired or rebuilt**.

## What if a model can't reach its budget?

It is marked **Over budget** on its card and in the batch counts — never silently shipped as passed. You can raise that category's number in [Profiles]({{ site.baseurl }}/docs/profiles/) and re-run, with the new profile named on the new card.

## Does Intake change my original files?

Never. Intake works on its own copies in `Assets/Intake/Output`; the Inbox originals are untouched.

## Does anything of Intake ship in my game?

No runtime component. Intake is Editor-only tooling; the output is ordinary meshes, materials, textures and prefabs that your project owns outright.

## What verification actually ran?

The full EditMode suite passes **32/32 in a clean install on Unity 2022.3 LTS** (fresh project, package as shipped), and every fixture is green on **Unity 6**, with zero compile errors in every final run.
