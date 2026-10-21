# Plan: Add Seed Patches Author Homepage Links

**Epic:** E0: Site Maintenance Baseline

## Summary

Add verified homepage links for Xingrui Yu and Ivor Tsang to both `[C21]` publication entries and the corresponding acceptance news.

**Decisions locked in:**
- Verify identities against the user-supplied CFAR/A*STAR affiliations and emails, using personal or institutional primary sources.
- Preserve all visible text, author order, contribution annotations, and publication metadata.
- Keep the local preview available for user review; no remote push is requested.

## Implementation and Verification

- [x] Verify both destination pages and record identity evidence.
- [x] Add the two author links to `index.html` News and Selected Publications, and `html/publications.html` Full Publications.
- [x] Verify link reachability, identical publication entries, unchanged text/annotations, and locally served content; run `git diff --check`.
- [x] Update `docs/PROGRESS.md` with outcome, verification, files, next steps, and blockers.

## Verified Destinations

- Xingrui Yu: https://xingruiyu.github.io/ — personal homepage identifies him as a CFAR/A*STAR research scientist and gives the matching `yu_xingrui@a-star.edu.sg` email.
- Ivor Tsang: https://www.a-star.edu.sg/cfar/about-cfar/management/prof-ivor-tsang — official A*STAR profile identifies Prof Ivor W. Tsang as CFAR director and contains the matching `ivor_tsang@a-star.edu.sg` email. Independent verification retrieved HTTP 200 and profile content. Also linked as his website in https://www.kcl.ac.uk/study-legacy/assets/fundingdb/astar-project-catalogue-26-27.pdf.

## Outcome

Added both author links to Selected Publications, Full Publications, and News (six anchors total). Both destinations returned HTTP 200. Removing just the six new anchors reproduces the original HTML exactly; the two publication entries remain identical. Both local preview pages returned HTTP 200 and the updated source. `git diff --check` passed. No browser visual inspection performed; no push/deployment performed.
