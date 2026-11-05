---
layout: home
title: Home
nav_order: 1
description: "Intake refines raw AI-generated models inside Unity: drop them in the Inbox, get grounded, budgeted prefabs out — with a report card for every model."
permalink: /
---

# Intake
{: .fs-9 }

Drop raw AI-generated models in the Inbox. Get **grounded, budgeted prefabs** out — with a **report card for every model**.
{: .fs-6 .fw-300 }

[Get started]({{ site.baseurl }}/docs/getting-started/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Buy on the Unity Asset Store](https://assetstore.unity.com/publishers/118262){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## The problem with raw generator output

Raw AI-generator output is not ready for your game. A simple prop commonly lands at 80,000 to 200,000 triangles where a game asset should carry 1,000 to 8,000 — floating off the ground, pivot in a corner, textures oversized, materials authored for the wrong render pipeline. The usual fix is hours of manual cleanup per model in a second application most Unity developers do not want to learn. Intake deletes that middle step: it works **inside the Unity Editor**, on files, with **no vendor account, no cloud call and no second application**. Intake uses no AI itself — it refines AI output.

- **Per-category triangle budgets** — Hero Prop 15,000 · Background Prop 4,000 · Environment Piece 30,000 by default, every number buyer-editable. A mesh that cannot reach its budget without collapsing is marked **Over budget** — never silently shipped as passed.
- **LOD chain and collider with every prefab** — LOD1 at 50% of LOD0, LOD2 at 25%, then cull, plus a convex MeshCollider generated from the LOD0 mesh.
- **Grounded, at the right size** — scale, pivot and grounding are normalised so prefabs land on the ground with the pivot at the base centre — every correction a number on the report card.
- **Materials in your pipeline** — texture sizes capped to the category ceiling, materials converted to your project's render pipeline (Built-in, URP or HDRP), and any channel Intake cannot map credibly is listed on the card as **Not converted** — never dropped silently.
- **An honest batch** — one bad model never fails the batch: a corrupt file fails that asset only, with its reason on its own report card. Skinned, rigged or animated meshes are routed to **Needs human pass**, untouched, with the detection evidence and the one next action on their card.

## See it work on the Messy Crate

The **Messy Crate Test** ships in the package: a deliberately raw crate at **184,512 triangles**, floating, corner pivot, two 4096×4096 textures, materials for the wrong pipeline. Intake returns it as a Ready prefab at **3,999 triangles** — grounded, LOD chain and convex collider attached, textures capped, materials converted — with the report card showing every number before and after. See [The Messy Crate Test]({{ site.baseurl }}/docs/messy-crate-test/).

## One home window

**Tools → Decnet Games → Intake** opens Intake Home: the Intake Queue, Report Cards, Profiles and Settings in one window, with a welcome screen whose quick actions run setup, start the Messy Crate Test, and open the documentation and support pages. See [The Home Window]({{ site.baseurl }}/docs/home-window/).

> Automated verification for v1.0.0: the full EditMode suite passes **32/32 in a clean install on Unity 2022.3 LTS**, and every fixture is green on **Unity 6**, with zero compile errors. Intake refines **static props and environment pieces** — it does not retopologise, and version 1 does not process glTF/GLB: a .glb file is detected and answered with the FBX instruction only. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
