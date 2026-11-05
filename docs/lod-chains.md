---
layout: default
title: LOD Chains
nav_order: 9
description: "Every ready prefab gets an LOD chain — LOD1 at 50% of LOD0, LOD2 at 25%, then cull — wired into an LODGroup on the prefab. Small assets ship as a single level, and the card says why."
---

# LOD Chains
{: .no_toc }

A budgeted mesh at one detail level is half the job. Every **Ready** prefab ships with an **LOD chain** generated from its refined LOD0 mesh:

- **LOD1** at **50%** of LOD0's triangle count.
- **LOD2** at **25%**.
- Then **cull** — beyond LOD2 the object stops rendering at distance, as the chain's final step.

The levels are saved as real mesh assets and referenced by the prefab's **LODGroup**, so the chain is ordinary Unity data your project owns — not a runtime trick Intake has to stay installed to perform.

## The small-asset exception

Assets at or under **500 triangles** ship as a **single level**: an LOD chain under that size buys nothing, and the report card **says why** the chain was skipped. The rule is the product's, the reason is on the card — nothing about a prefab's structure is left for you to reverse-engineer.

LOD behaviour is part of each category [profile]({{ site.baseurl }}/docs/profiles/), alongside the budget and the texture ceiling.
