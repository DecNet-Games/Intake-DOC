---
layout: default
title: Report Cards
nav_order: 13
description: "Every model gets a report card: its classification, the profile it was judged against, the budget verdict, and every change with before/after values — plus per-batch Markdown and JSON exports."
---

# Report Cards
{: .no_toc }

The report card is Intake's core promise: **nothing happens to your model off the record.** Every processed asset gets a card, and the card is complete whether the news is good or bad.

## What a card records

- The asset's **classification** and outcome — **Ready**, **Over budget**, **Needs human pass**, or **Failed**, each with its reason.
- The **profile it was judged against** (category, budget, ceilings), by name.
- **Triangles before and after**, and the budget verdict.
- The **LOD chain** produced — or, for a small asset, why it shipped as a single level.
- The **collider result**, with the hull's triangle count.
- **Scale, pivot and grounding corrections**, as numbers.
- **Texture caps applied** and the **material conversion** record — including every channel listed as **Not converted**.
- For a reduced mesh, the honesty line in full: *"This mesh was reduced in triangle count to meet the budget. A decimated mesh is not a retopologised mesh — it keeps its source topology character, reduced."*
- For a routed asset (**Needs human pass**), the **detection evidence** and the **one next action**.

## Batch exports

Per batch, Intake writes **Markdown and JSON exports** of the cards, and the batch summary states the counts plainly — ready, over budget, needs human pass, failed. The exports are the reviewable record of a run: what went in, what came out, and what a human still owes. Cards are browsable in the Home window's [Report Cards section]({{ site.baseurl }}/docs/home-window/).
