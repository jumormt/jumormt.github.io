# Summary: Visitor Map Footer Repair

**Date:** 2026-07-19
**Plan:** `docs/plans/2026-07-19-03-visitor-map-footer.md`
**Tags:** visitor-map, clustrmaps, busuanzi, graceful-degradation, static-site

> **Superseded later on 2026-07-19:** ClustrMaps was subsequently confirmed to serve a domain-parking page over HTTP and refuse HTTPS connections. Plan `docs/plans/2026-07-19-08-historical-globe-counter-fix.md` replaced the dead live loader with an animated archived-map globe and raw, host-aware Busuanzi counting; plan `docs/plans/2026-07-19-09-canvas-globe-refinement.md` then upgraded the flat animation to Canvas sphere projection.

## What Was Built

The homepage footer now uses a responsive visitor card with a non-blocking live ClustrMaps loader, the existing ClustrMaps data token, and a dated archived map fallback. The Busuanzi counter uses explicit HTTPS and native JavaScript while retaining the historical `+20000` adjustment.

## Key Decisions

- **Preserve identity, not just appearance:** The original ClustrMaps token remains attached to the live loader so restoring service does not create a new dataset.
- **Keep a truthful fallback:** A verified 23 February 2026 Wayback snapshot is shown and dated while the live endpoint is unavailable; it is automatically hidden when a live map renders.
- **Avoid render blocking:** The external map script is loaded dynamically with an eight-second availability fallback, so a third-party outage cannot stall the homepage.

## Lessons Learned

### What Worked Well

- Checking DNS and HTTP reachability separately revealed that the commonly copied CDN hostname is no longer valid while the root service hostname still resolves.
- Searching the Wayback CDX index by the exact data token recovered a recent historical image without changing the tracking identity.

### What Didn't Work / Pitfalls

- Merely replacing the old image with the widely copied `cdn.clustrmaps.com` script would still fail because that hostname currently returns NXDOMAIN.
- The old visit-offset code silently depended on jQuery even though no jQuery script was loaded.
- The installed Snap Firefox could not create screenshots, including for `about:blank`, so visual automation was not usable in this environment.

### Surprises

- The map failure combined three causes: protocol-relative URLs break direct-file preview, the static service was unreachable, and the page-view adjustment threw because `$` was undefined.

## Reusable Patterns

- **Identity-preserving fallback:** Keep the original third-party identifier in a non-blocking live loader and pair it with a clearly dated, verified archive snapshot.
- **Dependency-free late data adjustment:** Observe an asynchronously populated counter with `MutationObserver`, then apply a historical offset exactly once.

## Recommendations for Similar Work

- Record third-party data tokens before changing embeds and never generate a replacement token unless a reset is explicitly intended.
- Verify DNS, endpoint reachability, and page dependencies before treating a widget failure as a CSS problem.
- Make external widgets non-blocking and provide honest loading/error states.
