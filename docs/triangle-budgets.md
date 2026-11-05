---
layout: default
title: Triangle Budgets
nav_order: 8
description: "Per-category budgets enforced by in-Editor decimation: Hero Prop 15,000, Background Prop 4,000, Environment Piece 30,000 — every number editable, and Over budget is a verdict, not a quiet pass."
---

# Triangle Budgets
{: .no_toc }

A raw generator prop at 80,000–200,000 triangles is not an asset yet; it is a cost. Intake enforces a **per-category triangle budget** on static props and environment pieces, by decimation inside the Editor.

## The shipped defaults

| Category | Triangle budget |
|---|---|
| Hero Prop | 15,000 |
| Background Prop | 4,000 |
| Environment Piece | 30,000 |

Every number is **editable in the Profiles section**, and the report card always names the profile an asset was judged against — a budget is a decision you can see, not a hidden constant.

## Honest outcomes

- A mesh that reaches its budget is **Ready** (subject to the rest of its card).
- A mesh that **cannot reach its budget without collapsing** is marked **Over budget**. Intake never silently ships it as passed — the verdict is on the card and in the batch counts.
- Reduction takes time on dense meshes: the Messy Crate's ~184,000 triangles take **roughly four minutes**. The run reports progress per asset while it works.

## The line on every card

Decimation is reduction, not retopology. The report card for every reduced mesh carries the product's own honesty line:

> "This mesh was reduced in triangle count to meet the budget. A decimated mesh is not a retopologised mesh — it keeps its source topology character, reduced."

Intake does not produce quad topology or clean edge flow, and reduced output is **not deformation-ready**. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
