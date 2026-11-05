---
layout: default
title: Installation
nav_order: 3
description: "Install Intake from the Unity Asset Store and run the one-click setup. Intake is sold exclusively through the Unity Asset Store."
---

# Installation
{: .no_toc }

## Asset Store only
{: .no_toc .text-delta }

Intake is sold and delivered **exclusively through the Unity Asset Store** (publisher: Decnet Games). There is no other download channel — if a copy of Intake came from anywhere else, it did not come from us.

## Install

1. Purchase Intake on the Unity Asset Store.
2. In Unity, open **Window → Package Manager**, select **My Assets**, download and import Intake into your project.
3. Open the window from **Tools → Decnet Games → Intake**. Everything Intake does lives in that one home window — see [The Home Window]({{ site.baseurl }}/docs/home-window/).
4. Run the [one-click setup]({{ site.baseurl }}/docs/one-click-setup/) once. Setup prepares the Inbox and Output folders (`Assets/Intake/Inbox`, `Assets/Intake/Output`) and the shipped profiles; your edits to those profiles persist across later setup runs.

## Requirements

- Unity **2022.3 LTS** or **Unity 6**.
- Windows or macOS (Editor). Intake is Editor-only tooling: no runtime component, nothing added to your player build.
- No third-party dependencies.
- Models to refine as **FBX or OBJ** files — see [Formats — FBX, OBJ and glTF]({{ site.baseurl }}/docs/formats/) for exactly how glTF files are handled in v1.

## Verified state

Automated verification for v1.0.0: the full EditMode suite passes **32/32 in a clean install on Unity 2022.3 LTS** (fresh project, the package copied in as shipped), and every fixture is green on **Unity 6** (6000.5.4f1) across the driver's own stage runs, with zero compile errors in every final run. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/) for the boundaries of the product itself.
