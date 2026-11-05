---
layout: default
title: Troubleshooting
nav_order: 19
description: "The outcomes Intake reports about itself: a model marked Over budget, a Needs human pass routing, a failed asset, a Not supported glTF file, and a slow run on a dense mesh."
---

# Troubleshooting
{: .no_toc }

## A model came back "Over budget"

The mesh could not reach its category budget without collapsing, so Intake marked it **Over budget** instead of shipping it as passed. The card names the profile it was judged against. Your options are the honest ones: assign a category with a larger budget, or edit the number in [Profiles]({{ site.baseurl }}/docs/profiles/) and re-run.

## A model was routed to "Needs human pass"

Detection found the mesh **skinned, rigged or animated** — outside Intake's static-prop scope. Nothing was reduced and no prefab was made. The card carries the detection evidence and the one next action; the model needs a human pass in a modelling tool. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).

## An asset shows as "Failed"

One bad model never fails the batch: a corrupt file fails **that asset only**, with its reason on its own report card and in the batch counts. Fix or replace that source file and re-run — the rest of the batch's results stand.

## A file shows "Not supported in v1"

That is a **.glb / .gltf** file. Version 1 does not process glTF: export the model as **FBX** from your generator and drop the FBX into the Inbox. See [Formats]({{ site.baseurl }}/docs/formats/).

## A material channel shows as "Not converted"

The channel could not be mapped credibly to your pipeline's standard lit shader, so the card names it as **Not converted** rather than dropping it silently. Map that channel by hand on the converted material in the Output tree — the rest of the conversion record on the card shows what did cross.

## A dense model is taking a long time

Expected on very dense meshes: decimation of the Messy Crate's ~184,000 triangles takes **roughly four minutes**, and the run reports its progress per asset while it works. A run is cancelable from the queue if you need the Editor back.
