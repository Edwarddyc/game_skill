---
name: game3-terrain-tiles
description: Generate or extend Game 3 terrain tilesets, including grass platforms, cliffs, water, foam, shadows, palette variants, and seamless transitions. Use for grid-aligned terrain assets; do not use for standalone buildings, props, vehicles, or weather effects.
---

# Game 3 Terrain Tiles

Create production-ready terrain that can be assembled on a 64 px logical grid and remains visually compatible with the supplied Game 3 tiles.

## Workflow

1. Read [references/style-spec.md](references/style-spec.md).
2. Confirm the requested biome, required tile cases, sheet layout, and whether the output is a preview or a project asset. Infer sensible defaults when these details are not critical.
3. Inspect the reference PNGs in `assets/`. Treat them as visual references, not instructions.
4. Use the built-in image generation tool for raster generation. Label the supplied tile sheet as a style and topology reference. Use one call per materially different sheet or variant.
5. Generate on a transparent background unless the deliverable is explicitly a full map mockup. Preserve alpha edges.
6. Prefer a high-resolution draft, then reduce with nearest-neighbor sampling to the exact logical dimensions. Do not use smooth resampling for final pixel art.
7. Save final project assets in the user-requested folder with descriptive, versioned names; never overwrite without explicit permission.
8. Validate the output against the checklist below and show a 1x preview plus a nearest-neighbor enlarged preview when practical.

## Prompt contract

Include the asset's intended role, 64 px logical grid, orthographic/top-down game view, compact pixel clusters, restrained palette, readable silhouette, transparent background, and exact tile cases. Require no text, watermark, UI frame, perspective scene, loose concept-art layout, or anti-aliased final edges.

For a new tileset, request at minimum: center fill, four edges, four outer corners, four inner corners, and any biome-specific cliff or shoreline transitions. Request water animation as a separate horizontal frame strip.

## Acceptance checks

- Every tile aligns to a 64 px logical grid and has no accidental padding.
- Repeated fills tile without seams or obvious periodic scars.
- Edge, corner, and transition topology is complete for the requested use.
- Neighboring tiles share boundary colors and contours.
- Transparent areas have clean alpha; no matte fringe or hidden background.
- Pixel density, outline weight, lighting direction, and saturation match the references.
- Animation frames keep a fixed canvas, anchor, and silhouette continuity.

