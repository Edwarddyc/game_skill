# Props and effects style specification

## Dominant target language

Normalize outputs toward the terrain/building family: 64 px logical grid, compact pixel clusters, limited palette, dark blue-green or brown outlines, upper-left lighting, readable silhouettes, and transparent PNG delivery.

## Reference routing

- `assets/roads2w.png`: road topology, width, shoulder colors, and dashed center marking. Original sheet is 512x192, an 8x3 logical grid.
- `assets/rock-cluster-256.png`: target rock silhouette, faceting, outline, and palette.
- `assets/rock-waterline-256.png`: waterline crop/grounding variant.
- `assets/tree-concept.png`: silhouette and foliage mass only. Do not reproduce its soft gradient background or dense high-resolution texture.
- `assets/car-concept.png`: vehicle anatomy and top-view proportions only. Do not reproduce its thick hand-drawn curves at final pixel scale.
- `assets/rain-concept.png`: motion direction or density only. Verify alpha independently; generate the final effect as an actual transparent overlay.

## Category sizing defaults

- Small prop: 64x64.
- Medium prop/cluster: 128x128 or 256x256, aligned to 64 px increments.
- Road sheet: exact 64 px cells.
- Vehicle: size to the established road lane, then add only the transparent safety margin needed for rotation or animation.
- Weather: power-of-two transparent tile or fixed-frame strip chosen for the engine integration.

## Consistency rule

When references disagree, gameplay scale and the terrain/building pixel language win. A concept reference controls subject identity, not rendering style.

