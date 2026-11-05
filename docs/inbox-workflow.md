---
layout: default
title: The Inbox Workflow
nav_order: 7
description: "Scan the Inbox, assign a category per model, run the batch: grounded, budgeted prefabs out, a report card per model, and per-asset failures that never fail the batch."
---

# The Inbox Workflow
{: .no_toc }

## 1. Drop and scan

Drop raw models into `Assets/Intake/Inbox`. Intake scans the folder and lists **every model with its real triangle count** — the census you judge the batch by before anything runs. Detection also classifies what Intake must not touch: a skinned, rigged or animated mesh is recognised at this stage.

## 2. Assign a category

Each model gets a category — **Hero Prop**, **Background Prop**, or **Environment Piece** — which selects the [profile]({{ site.baseurl }}/docs/profiles/) it will be judged against: its triangle budget, texture ceiling, and LOD behaviour. The report card always names the profile an asset was judged against.

## 3. Run Intake

**Run Intake** processes the queue. The run is cancelable and reports its progress **per asset**. What comes back, per model, lands in `Assets/Intake/Output`:

- A **prefab** built from the refined mesh, its [LOD chain]({{ site.baseurl }}/docs/lod-chains/) and a [convex collider]({{ site.baseurl }}/docs/colliders/).
- **Scale, pivot and grounding** normalised — see [Scale, Pivot & Grounding]({{ site.baseurl }}/docs/scale-pivot-grounding/).
- **Textures capped and materials converted** to your render pipeline, on Intake's own copies — your originals are never modified. See [Textures & Materials]({{ site.baseurl }}/docs/textures-and-materials/).
- A **[report card]({{ site.baseurl }}/docs/report-cards/)** listing every change with before/after values.

## 4. The batch stays honest

The batch summary states the counts plainly — **ready, over budget, needs human pass, failed** — and the batch never inherits one model's fate:

- A **corrupt file fails that asset only**, with its reason on its own report card.
- A mesh that cannot reach its budget without collapsing is marked **Over budget** — never silently shipped as passed.
- A **skinned, rigged or animated** mesh is classified **Needs human pass**: no reduction, no LOD chain, no prefab — with the detection evidence and the one next action on its report card.
- A **.glb / .gltf** file is listed **Not supported in v1** with the FBX instruction — see [Formats]({{ site.baseurl }}/docs/formats/).
