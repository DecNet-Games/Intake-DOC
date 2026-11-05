---
layout: default
title: The Messy Crate Test
nav_order: 15
description: "The shipped sample: a deliberately raw crate — 184,512 triangles, floating, corner pivot, two 4096×4096 textures, wrong-pipeline materials — returned at 3,999 triangles with its report card."
---

# The Messy Crate Test
{: .no_toc }

The Messy Crate Test ships in the package (importable after [setup]({{ site.baseurl }}/docs/one-click-setup/)) so the first run you ever make is against a model whose problems are known to the triangle.

## What goes in

- **184,512 triangles** for a crate — a background prop carrying hero money.
- **Floating**, with its **pivot in a corner**.
- **Two 4096×4096 textures**, far over the Background Prop ceiling.
- **Materials authored for the wrong render pipeline.**
- The shipped sample file is an **OBJ** — the window imports whatever the sample folder holds, and the sample's numbers above are its real census.

## What comes out

A **Ready prefab at 3,999 triangles** — inside its 4,000 Background Prop budget — **grounded** on the sample scene's ground, with its [LOD chain]({{ site.baseurl }}/docs/lod-chains/) and [convex collider]({{ site.baseurl }}/docs/colliders/) attached, **textures capped**, and **materials converted** to your project's pipeline. The reduction takes roughly four minutes for a mesh this dense; the run reports progress while it works.

## The card

The crate's [report card]({{ site.baseurl }}/docs/report-cards/) shows **every number before and after**: triangles in and out, the profile it was judged against, the scale/pivot/grounding corrections, the texture caps, the conversion record, the collider result — and the honesty line every reduced mesh carries, that a decimated mesh is not a retopologised mesh.

That sequence — raw in, budgeted and grounded out, everything on the card — is the demo, the onboarding, and the product.
