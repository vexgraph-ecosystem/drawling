# drawling — R5 drawing studio

**Role:** R5 Interactable — GIMP/Krita/FlipaClip target: layers, brushes,
frame-by-frame animation, canvas-first workflow.
**Status:** stub (LICENSE only; no studio code yet).

## What it is
`drawling` is the end-user painting and 2D animation application: brush
engines on `graphvex` raster/SDF, layer UI on `darling-framework`,
supervised as an R1 `Application` by the `hotcwap` Kernel.

## Depends on (Vertical Integration Law allowlist)
Borrows shapes from R1–R4 (arenas, windows, GPU, UI) to build; owns no
OS/window/memory management itself. Standalone-capable or Kernel-registered.

## Layout
- Studio (future): `src/` — canvas, layers, brush engines, timeline.
- Tests: the shared `tests/` repo hosts a `tests/drawling/` partition (mirrored
  per unit, the Test Tree Mirror Law); no test file lives inside this repo's
  source directories (the Test Segregation Law).

## Laws that govern work here
- Constitution: the universal [`preferences.md`](../../ecosystem/vexspoke/preferences.md) (canonical file; the workspace root links to it).
- Commits land in THIS repo root, one cohesive unit each; never push unless asked.
- One public class per `.h`/`.c` pair, `(*ptr).field` (never `->`), dest-last
  params, `-Wall -Wextra -Werror`.
