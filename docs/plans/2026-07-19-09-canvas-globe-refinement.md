# Plan: Refine the Historical Globe with Canvas Projection

**Epic:** E0: Site Maintenance Baseline

## Summary

Replace the flat scrolling illusion with a real Canvas sphere projection inspired by the supplied reference site's archived SVG globe renderer. Project the site's own archived world map and red visitor dots onto a rotating sphere with curvature and lighting, while retaining the current CSS globe as a no-script/image-failure fallback.

**Decisions locked in:**
- Do not reuse the reference site's embedded visitor coordinates.
- Use the site's verified 23 February 2026 map snapshot as the only geographic data texture.
- Render at 150×150 to match the reference footprint and current compact footer.
- Keep the existing archive link, historical label, raw production Busuanzi behavior, and local count suppression.
- Respect `prefers-reduced-motion` by drawing one frame without continuous rotation.

---

## Phase 1: Canvas Globe Rendering

### [x] Task 1.1: Add the Canvas surface
- [x] Add an accessible, noninteractive 150×150 canvas inside the existing archive link.
- [x] Keep the CSS background globe visible as a fallback below the canvas.

### [x] Task 1.2: Implement sphere projection
- [x] Load the archived map texture and crop out its title/count header.
- [x] Project vertical texture slices onto the visible hemisphere using spherical curvature.
- [x] Animate longitude rotation and add edge shading/highlight for depth.
- [x] Stop continuous animation when reduced motion is requested.

## Phase 2: Verify and Document

### [x] Task 2.1: Verify rendering safeguards
- [x] Confirm the renderer uses only the site's archived map URL.
- [x] Confirm the canvas and fallback both remain inside the full-map link.
- [x] Confirm visitor count behavior is unchanged.
- [x] Confirm local preview, JavaScript syntax, and `git diff --check` pass.

### [x] Task 2.2: Close the LDD session
- [x] Mark plan tasks complete.
- [x] Update `docs/PROGRESS.md` with status, tests, files, next steps, and blockers.

## Verification
- [x] Globe uses sphere projection rather than flat background scrolling.
- [x] Archived red visitor points remain part of the rotating texture.
- [x] Reference-site visitor coordinates are not reused.
- [x] CSS fallback and reduced-motion behavior remain available.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` is updated with results.
