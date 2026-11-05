---
layout: default
title: One-Click Setup
nav_order: 6
description: "Setup prepares the Inbox and Output folders and the shipped category profiles — idempotently, so your profile edits survive every later setup run."
---

# One-Click Setup
{: .no_toc }

Setup is the welcome screen's first quick action. It prepares what the pipeline needs inside your project:

- The **Inbox** folder — `Assets/Intake/Inbox`, where raw models are dropped.
- The **Output** folder — `Assets/Intake/Output`, where refined prefabs, their meshes, materials and textures are written. Your original Inbox files are **never modified**; Intake works on its own copies.
- The shipped **category profiles** (Hero Prop, Background Prop, Environment Piece) with their default budgets and ceilings.

## Your edits persist

Setup is safe to run again. Buyer edits to profiles — a changed budget, a duplicated profile, your own numbers — **persist across setup**: re-running setup recognises the existing state instead of resetting your tuning to the shipped defaults. This behaviour is covered by an automated test in the shipped suite.

## The sample, on demand

Setup also makes the **Messy Crate Test** available from the welcome screen — the shipped sample described in [The Messy Crate Test]({{ site.baseurl }}/docs/messy-crate-test/). Importing the sample is your choice, not a setup side effect you discover later.
