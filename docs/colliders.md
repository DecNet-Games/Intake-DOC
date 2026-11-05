---
layout: default
title: Convex Colliders
nav_order: 10
description: "Every ready prefab gets a convex MeshCollider generated from its LOD0 mesh — so a refined prop can be placed, stacked and collided with the moment it lands in a scene."
---

# Convex Colliders
{: .no_toc }

A prefab you cannot collide with is a picture. Every **Ready** prefab Intake produces carries a **convex MeshCollider generated from the LOD0 mesh** — the full-detail refined mesh, not an LOD level — so the prop can be placed, stacked, walked into and shot at the moment it lands in a scene.

The collider result is a field on the asset's [report card]({{ site.baseurl }}/docs/report-cards/): the Messy Crate's card, for example, records its collider result as **Pass**, with the hull's triangle count recorded alongside it. If a hull cannot be generated for a mesh, the failure is graceful and stated — a card that says what happened, not a prefab that silently ships without collision.
