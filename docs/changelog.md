---
layout: default
title: Changelog
nav_order: 20
description: "Intake 1.0.0 — the initial release: folder-in, prefab-out intake with per-category budgets, LOD chains, convex colliders, grounding, pipeline material conversion, and report cards."
---

# Changelog
{: .no_toc }

## 1.0.0 — initial release

- Intake Home — one Editor window (Intake Queue, Report Cards, Profiles, Settings) with a welcome screen, one-click setup, and verification.
- Folder-in, prefab-out intake: Inbox scan with real triangle counts, per-model category assignment, cancelable batch runs with per-asset progress, and per-asset failures that never fail the batch.
- Per-category triangle budgets enforced by in-Editor decimation (Hero Prop 15,000 · Background Prop 4,000 · Environment Piece 30,000 — every number buyer-editable), with Over budget as an explicit verdict.
- LOD chain generation (LOD1 at 50%, LOD2 at 25%, then cull) and a convex MeshCollider generated from the LOD0 mesh for every ready prefab; assets at or under 500 triangles ship as a single level, with the reason on the card.
- Scale, pivot and grounding normalisation — prefabs land on the ground at the right size, pivot at the base centre, every correction a number on the report card.
- Texture caps to the category ceiling (2048 or 1024 by profile) on Intake's own copies, and material conversion to the project's render pipeline (Built-in, URP or HDRP) with unmapped channels named as Not converted.
- Per-asset report cards (every change with before/after values, the profile judged against, and the decimation honesty line) plus per-batch Markdown and JSON exports and plain batch counts — ready, over budget, needs human pass, failed.
- Routing for what Intake must not touch: skinned, rigged or animated meshes classified Needs human pass with detection evidence and the one next action; glTF/GLB files detected and answered with the FBX instruction (not processed in v1).
- Messy Crate Test sample: a raw 184,512-triangle crate returned at its 4,000 budget (3,999 triangles), grounded, with LOD chain, convex collider, capped textures and converted materials.
- Documentation set: quick-start, full reference (profiles, report-card fields, warnings, naming rules, pipeline conversion maps), "what v1 is not".
- 32 automated EditMode tests (NUnit): full suite green 32/32 in a clean install on Unity 2022.3 LTS, every fixture green on Unity 6, zero compile errors.
- Unity 2022.3 LTS and Unity 6 · Windows and macOS (Editor) · Editor-only, no runtime component · No third-party dependencies.
