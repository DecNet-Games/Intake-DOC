---
layout: default
title: Getting Started
nav_order: 2
description: "From the Asset Store download to your first refined prefab: install Intake, run setup, drop a model in the Inbox, and read its report card."
---

# Getting Started
{: .no_toc }

Intake works in one Editor window and one loop: **scan** the Inbox, **assign** a category per model, **run** the batch, **read** the report cards. This section takes you from the Asset Store download to your first grounded, budgeted prefab.

## The path

1. [Install]({{ site.baseurl }}/docs/installation/) the package from the Unity Asset Store.
2. Follow the [Quick Start]({{ site.baseurl }}/docs/quick-start/): open Intake Home, run setup, and try the Messy Crate Test.
3. Learn the one window in [The Home Window]({{ site.baseurl }}/docs/home-window/), then the full flow in [The Inbox Workflow]({{ site.baseurl }}/docs/inbox-workflow/).

## What Intake needs from you

- A Unity **2022.3 LTS** or **Unity 6** project, on Windows or macOS (Editor). Intake is Editor-only tooling — it adds nothing to your player build.
- Models as **FBX or OBJ** files. Version 1 does not process glTF/GLB: a .glb or .gltf file in the Inbox is detected, listed as **Not supported in v1**, and answered with one instruction — export the model as FBX from your generator and drop the FBX in the Inbox. See [Formats — FBX, OBJ and glTF]({{ site.baseurl }}/docs/formats/).

## The honest frame, up front

Intake refines **static props and environment pieces**. It does not retopologise, does not produce quad topology or clean edge flow, and its output is not deformation-ready — the report card for every reduced mesh says so, in those words. Skinned or character meshes are routed to a human pass, never reduced. Intake uses **no AI**: it processes files locally, identically, whether the model came from Meshy, Tripo, Rodin, Hunyuan, TRELLIS, a collaborator's export, or a hand-made file. The full boundary list is in [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
