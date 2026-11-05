---
layout: default
title: Formats — FBX, OBJ and glTF
nav_order: 14
description: "Version 1 reads FBX and OBJ. glTF/GLB is detected in the Inbox, listed as Not supported in v1, and answered with the FBX instruction only — Intake does not import or process glTF."
---

# Formats — FBX, OBJ and glTF
{: .no_toc }

## What v1 reads

**FBX and OBJ.** Intake processes files, not services, so it works identically on output from Meshy, Tripo, Rodin, Hunyuan, TRELLIS, a collaborator's export, or a hand-made model in either format.

## How glTF is handled — exactly

Version 1 **does not import or process glTF/GLB**. There is no partial pipeline and no silent conversion:

1. A `.glb` or `.gltf` file dropped in the Inbox is **detected** during the scan.
2. It is listed in the queue as **Not supported in v1**.
3. It is answered with **one instruction**: export the model as FBX from your generator and drop the FBX in the Inbox.

That is the whole of Intake's glTF behaviour in v1, stated here, in the listing copy, and in [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/) — so the boundary is a fact you can plan around, not a surprise mid-batch. The file does not fail your batch, and it is never modified.
