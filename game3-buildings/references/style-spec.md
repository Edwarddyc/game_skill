# Building style specification

## Observed source system

- Canonical sprite variants: 64x64 and 128x128 RGBA PNG.
- View: compact top-down 3/4 presentation with the roof dominant and the front façade visible.
- Shape language: rounded rectangular footprint, chunky roof cap, centered entry, symmetrical major masses, selective asymmetry in tiny props.
- Line and color: dark brown contour, salmon-red roof, cream walls, deep red door, warm highlights and compact shadow clusters.
- Detail density: strong silhouette first; small roof blocks and façade accents second.

## Scaling policy

- Treat 128x128 as the preferred generation/master canvas when both sizes are needed.
- `64-crisp`: nearest-neighbor reduction and manual cleanup at 1x.
- `64-smooth`: filtered presentation variant only; do not use as the canonical pixel asset when crisp gameplay rendering is required.
- Keep identical anchor, proportions, and transparent margins across variants.

## Customization levers

Safely vary roof palette, wall material, faction emblem shape, door treatment, one signature prop, footprint, and upgrade tier. Keep camera angle, outline weight, light direction, pixel density, and door-scale language fixed across a collection.

