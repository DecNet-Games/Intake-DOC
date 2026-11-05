---
layout: default
title: Scale, Pivot & Grounding
nav_order: 11
description: "Generator models arrive floating, at the wrong size, with the pivot in a corner. Intake normalises scale, pivot and grounding so prefabs land on the ground at the right size — every correction a number on the card."
---

# Scale, Pivot & Grounding
{: .no_toc }

Three of the most recognisable tells of raw generator output: the model **floats** off the ground, its **scale** is arbitrary, and its **pivot sits in a corner** instead of anywhere useful. Intake normalises all three for every refined prefab:

- **Grounding** — the prefab lands **on the ground**, not hovering above it or sunk into it.
- **Pivot** — moved to the **base centre** of the object, so rotation and placement behave the way a level designer expects.
- **Scale** — normalised to the right size for the category, with facing preserved.

None of this is silent. **Every correction is a number on the report card** — the scale factor applied, the pivot offset, the grounding adjustment — so you can see exactly what Intake decided about your model and overrule it with knowledge, not archaeology. The full field list is in [Report Cards]({{ site.baseurl }}/docs/report-cards/).
