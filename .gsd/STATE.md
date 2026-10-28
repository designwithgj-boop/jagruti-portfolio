# STATE: Jagruti Profile Page

## Current Position
- **Phase**: 1
- **Plan**: 01
- **Status**: Planning Phase 1

## Key Decisions & Constraints
- Single-file `index.html` (all HTML, CSS, JS contained without external build tools).
- Stage scaling: `transform: scale(min(100vw/1440, 100vh/960))` centered in fixed viewport.
- All motion driven by a single hidden Web Animation clock `clockDriver.animate(...)` through `requestAnimationFrame`.
- Inter font with full weights (400, 500, 520, 600, etc.).
- Color tokens matched exactly to prompt specifications.

## Blockers / Concerns
- None.
