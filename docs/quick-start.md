---
layout: default
title: Quick Start
nav_order: 4
description: "The Messy Crate path: run setup, start the shipped test, and watch a raw 184,512-triangle crate come back as a Ready prefab at 3,999 triangles with its report card."
---

# Quick Start
{: .no_toc }

The Messy Crate Test is the quick start. It ships in the package so your first Intake run is against a model whose problems are known exactly.

## The path

1. Open **Tools → Decnet Games → Intake** and run [setup]({{ site.baseurl }}/docs/one-click-setup/) from the welcome screen.
2. Start the **Messy Crate Test** from the welcome screen's quick actions. The crate is deliberately raw: **184,512 triangles**, floating, pivot in a corner, two 4096×4096 textures, materials authored for the wrong render pipeline.
3. Watch it move through the [Inbox workflow]({{ site.baseurl }}/docs/inbox-workflow/): scanned with its real triangle count, categorised as a Background Prop, and refined against that profile's **4,000-triangle budget**. A mesh this dense takes minutes, not seconds — roughly four minutes for the crate — and the run reports its progress per asset while it works.
4. Read the result in the Output: a **Ready prefab at 3,999 triangles**, grounded on the sample scene's ground, [LOD chain]({{ site.baseurl }}/docs/lod-chains/) and [convex collider]({{ site.baseurl }}/docs/colliders/) attached, textures capped, materials converted to your pipeline.
5. Open its [report card]({{ site.baseurl }}/docs/report-cards/) — every change, every number, before and after, including the line every reduced mesh carries: a decimated mesh is not a retopologised mesh.

Then drop your own models into `Assets/Intake/Inbox` and run the same loop. The full sample breakdown is in [The Messy Crate Test]({{ site.baseurl }}/docs/messy-crate-test/).
