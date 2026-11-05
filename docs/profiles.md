---
layout: default
title: Profiles
nav_order: 16
description: "The category profiles — triangle budget, texture ceiling and LOD behaviour per category — are yours to edit and duplicate, and your edits persist across setup."
---

# Profiles
{: .no_toc }

A **profile** is the set of numbers a category is judged against. The shipped profiles are **Hero Prop**, **Background Prop**, and **Environment Piece**, carrying the defaults:

| Category | Triangle budget | Texture ceiling |
|---|---|---|
| Hero Prop | 15,000 | by profile (2048 or 1024) |
| Background Prop | 4,000 | by profile (2048 or 1024) |
| Environment Piece | 30,000 | by profile (2048 or 1024) |

Each profile also carries its category's LOD behaviour (see [LOD Chains]({{ site.baseurl }}/docs/lod-chains/)).

## Yours to edit

**Every number is editable** in the Home window's Profiles section, and profiles can be **duplicated** to make your own variants — a "Set Dressing" profile with a 2,000 budget is a duplicate and two edits, not a feature request. The report card always names the profile an asset was judged against, so a tuned profile's decisions stay auditable.

## Edits persist

Your profile edits **persist across setup runs**: re-running [setup]({{ site.baseurl }}/docs/one-click-setup/) recognises your numbers instead of resetting them to the shipped defaults. This is covered by an automated test in the shipped suite — your tuning is your project's data, not a cache Intake feels free to clear.
