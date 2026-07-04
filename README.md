# Tessera — Tile Pattern Generator

A black-and-white generative tile pattern engine with two switchable grid systems:

- **Square** — a diamond-in-square Truchet tile, with four independently colored corner triangles per cell. Diamonds interlock across neighboring cells to form larger emergent forms.
- **Hex** — an axial-coordinate hex grid (per [redblobgames.com/grids/hexagons](https://www.redblobgames.com/grids/hexagons/)), each cell split into six triangular wedges radiating from its center.

Both grids share one seeded PRNG (mulberry32) and an **Order ↔ Chaos** control: at 0, fill is fully deterministic from coordinate parity (flowing, architectural); at 1, it's pure random noise.

## Features

- Square + hex grid modes, switchable live
- Seeded, reproducible generation — same seed always produces the same field
- Seed stepper (±) for stepping through variations, plus manual seed entry
- Order ↔ Chaos, cell size, fill balance, and diamond-scale controls
- Play / Pause auto-generate, with an adjustable cycling speed — plays automatically on load
- Canvas sizing guarantees no cell or hex is ever cut off at the edges
- SVG and high-resolution PNG export
- Single HTML file, no build step, no dependencies

## Tech

Vanilla HTML/CSS/JS. No frameworks, no bundler. `mulberry32` for seeded randomness. SVG for rendering, `<canvas>` only as an intermediate step for PNG export.

## Deployment

Static site — deploys as-is on Netlify (see `netlify.toml`) with continuous deployment from this repo.

## Author

Joe Kendsersky — [axisbim.io](https://axisbim.io)

## License

© Joe Kendsersky / Axis BIM. All rights reserved.
