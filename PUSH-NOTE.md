# PUSH NOTE — Intake-DOC (built 2026-11-05, local only, NOT pushed)

## What this folder is

The complete, push-ready source tree for Intake's documentation site, built to the Decnet house "-DOC" pattern (structure/config mirrored from MergeGuard-DOC / AgentProof-DOC / SteamDeck-DOC / ShipSheet-DOC):

- Just the Docs Jekyll site via `remote_theme` (no `theme:` gem key, no `just-the-docs` gem in the Gemfile — the pairing that fixed the two known GitHub Pages errors: "The just-the-docs theme could not be found" and "The github-pages gem can't satisfy your Gemfile's dependencies").
- 21 content pages: Home + Getting Started + Installation + Quick Start + The Home Window + One-Click Setup + The Inbox Workflow + Triangle Budgets + LOD Chains + Convex Colliders + Scale, Pivot & Grounding + Textures & Materials + Report Cards + Formats — FBX, OBJ and glTF + The Messy Crate Test + Profiles + What v1 Is Not + FAQ + Troubleshooting + Changelog + Support.
- **No media in this tree, by design** (the MergeGuard-DOC precedent: zero screenshots, text-first documentation). Documentation never ships invented imagery, and the pages are written so they do not depend on any image; if the marketing stage later wants frames under `assets/`, they come from the product's real capture record only.
- Content sourced ONLY from the verified record: the prep listing copy (`../../intake-prep/LISTING-COPY.md` — every capability line is one of its SPEC-13 allowed claims; the copy itself makes no claim that depends on the interactive capture pass) and the build evidence in `~/workspace/laptop-runs/intake-src/GAP-REPORT.md` (full suite 32/32 in a clean install on Unity 2022.3.22f1; every fixture green on Unity 6 6000.5.4f1 across the driver's own stage runs; compile errors 0). The GAP report's named exception is respected throughout: the V-* human click-throughs are still owed, so the site claims only the test-evidenced verification above — never a human GUI pass. **Binding fences held everywhere:** glTF/GLB is documented as detected + answered with the FBX instruction ONLY (v1 never imports or processes glTF); no retopology, quad-topology, deformation-readiness or UV-repair claims; Intake is never called "AI-powered" (it uses no AI — it refines AI output); scope is static props + environment pieces only, with skinned/rigged/animated meshes documented as routed to Needs human pass.
- No product Asset Store URL exists yet (no portal draft for Intake has been created — draft creation follows the capture stage), so Home/Installation link the Decnet Games publisher page (118262) — swap in the product URL after the listing goes live, as with the other -DOC trees.

## Exact repo to create

- **Name:** `Intake-DOC`
- **Owner:** `DecNet-Games` (GitHub org account)
- **Visibility:** public (required for GitHub Pages on this setup)
- **Live URL once Pages is on:** https://decnet-games.github.io/Intake-DOC/ (matches the `baseurl: "/Intake-DOC"` already set in `_config.yml`)

## Push route (do this from the laptop, per the standing no-card-spam rule)

Bulk pushes go via laptop git over SSH — never the GitHub connector.

1. BOSS creates the empty repo `DecNet-Games/Intake-DOC` on GitHub (no README, no .gitignore — this tree is the repo content).
2. Copy this folder's contents to the laptop clone location, then: `git init` (if needed) → `git add .` → `git commit` → the final `git push` is BOSS's own ~10-second action at his terminal (laptop git credentials only work interactively — known constraint).
3. On GitHub: repo **Settings → Pages → Build and deployment → Source: GitHub Actions** (the standard github-pages workflow), or "Deploy from a branch" → `main` / root if Actions is unavailable. The other -DOC repos run on the same org setup — mirror whichever source they use.
4. After the first successful build, verify:
   - the live URL loads with the Just the Docs theme (no theme error),
   - nav order: Home, Getting Started, Installation, Quick Start, The Home Window, One-Click Setup, The Inbox Workflow, Triangle Budgets, LOD Chains, Convex Colliders, Scale, Pivot & Grounding, Textures & Materials, Report Cards, Formats — FBX, OBJ and glTF, The Messy Crate Test, Profiles, What v1 Is Not, FAQ, Troubleshooting, Changelog, Support.
5. Only after the site is live: apply the house-format description (`../DESCRIPTION-HOUSE.md`) to Intake's portal draft once that draft exists — its link line carries `DOCUMENTATION → https://decnet-games.github.io/Intake-DOC/` (dead-link rule: never publish the link before the site resolves).

## What remains

- Repo creation + push + Pages enable: BOSS-side steps above (by design — this build stopped at a complete local tree, per instructions).
- Portal draft: not yet created for Intake (it follows the capture stage in the pipeline); the plain portal text is `../../intake-prep/LISTING-COPY.md`, and `../DESCRIPTION-HOUSE.md` is the prepared house-format replacement for when the site is live.
- Media: not required for the site to be complete or correct; any future `assets/` frames come from the real capture record (see the capture RESUME notes in `../work/`), never from invented imagery.
- Nothing in the tree itself: content, config and Gemfile are complete and internally verified (page count, front matter, nav order checked against disk).
