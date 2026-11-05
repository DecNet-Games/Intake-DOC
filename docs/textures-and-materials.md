---
layout: default
title: Textures & Materials
nav_order: 12
description: "Texture sizes capped to the category ceiling on Intake's own copies, and materials converted to your project's render pipeline — with unmapped channels named as Not converted, never dropped silently."
---

# Textures & Materials
{: .no_toc }

## Texture caps

Generator textures arrive oversized — the Messy Crate carries two 4096×4096 textures for a background prop. Intake **caps texture sizes to the category ceiling** (**2048 or 1024**, by profile) — on **Intake's own copies**. Your original Inbox files are never modified; the caps apply to the copies in the Output tree.

## Material conversion

Materials are converted to **your project's active render pipeline — Built-in, URP or HDRP** — as a faithful mapping to the pipeline's standard lit shader. A converted material is a working starting point in the right pipeline, not a claim of perfect reproduction of the source look.

## Channels are named, not dropped

A channel Intake cannot map credibly is listed on the report card as **Not converted**. No channel is dropped silently: if a map did not make the crossing, the card says which one and the conversion record stays complete. See [Report Cards]({{ site.baseurl }}/docs/report-cards/).

## UVs: preserved, not repaired

Source UVs are **preserved and checked — not repaired or rebuilt**. Intake does not claim UV repair anywhere; if a model's UVs are broken, that is a fact about the source file, not something Intake quietly papers over. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
