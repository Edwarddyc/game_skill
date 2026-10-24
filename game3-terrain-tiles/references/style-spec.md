# Terrain style specification

## Observed source system

- Logical unit: 64x64 px.
- Main sheets: 576x384 px, equivalent to a 9x6 logical grid.
- Visual language: compact hand-pixeled clusters, dark blue-green contour, lime/yellow-green grass, cool gray or warm brown cliff faces, small high-frequency grass accents.
- View: orthographic/top-down platform map, not side-scrolling perspective.
- Lighting: highlights toward upper-left; darkest contour and crevices toward lower/right edges.
- Water support assets: 64x64 flat water color, 192x192 shadow, and a 3072x192 foam strip that implies 16 frames of 192x192.

## Reference routing

- Use `assets/tilemap-color1.png` for topology, edge vocabulary, pixel density, and cool cliff palette.
- Use `assets/tilemap-brown.png` only when a warm earth cliff is requested.
- Use `assets/water-foam.png` only for animation rhythm and fixed-frame alignment.

## Palette customization

Change hue families while preserving value roles: darkest outline, deep crevice, mid body, bright body, and sparse highlight. Keep adjacent transition tiles on the same palette. Avoid gradients, airbrush texture, photographic noise, and single-pixel speckle unrelated to the existing cluster rhythm.

## Deliverable patterns

- Static biome tiles: transparent PNG sheet on a 64 px grid.
- Water: separate base fill and animated foam strip.
- Palette variant: identical topology and alpha, colors changed only.
- Map preview: separate composite image; never substitute it for the usable sheet.

