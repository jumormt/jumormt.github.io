# jumormt.github.io Development Progress

## Current Epic
**E0: Site Maintenance Baseline** — Maintain Xiao Cheng's static academic homepage with reliable cross-session documentation for content, publication, service, and asset updates.

## Epics
- [x] E0: Site Maintenance Baseline
- [ ] E1: Future content updates and site improvements

## Plans Index (active/recent — see `SESSION-LOG-ARCHIVE.md` for earlier plans)
| Date | Plan | Epic | Status | Notes |
|------|------|------|--------|-------|
| 2026-07-19 | [merged-visitor-map](plans/2026-07-19-13-merged-visitor-map.md) | E0 | done | Replaced the two-map footer with one archived historical map plus live green coordinate overlays and graceful failure behavior. |
| 2026-07-19 | [live-visitor-map](plans/2026-07-19-12-live-visitor-globe.md) | E0 | done | Introduced the replacement live dataset and visible archive; its interim two-card layout was superseded by the merged-map plan. |
| 2026-07-19 | [supervision-additions](plans/2026-07-19-11-supervision-additions.md) | E0 | done | Added Thanakit Rattikanchalakorn to Current and Jianing Wang to Alumni with their supplied status details. |
| 2026-07-19 | [comp3050-feedback-summary](plans/2026-07-19-10-comp3050-feedback-summary.md) | E0 | done | Published a privacy-safe aggregate/paraphrased COMP3050 feedback page; the internal PDF, demographics, and response-level comments remain private. |
| 2026-07-19 | [canvas-globe-refinement](plans/2026-07-19-09-canvas-globe-refinement.md) | E0 | done | Upgraded the flat scrolling fallback to a 150×150 Canvas sphere projection with curved texture slices, lighting, reduced-motion support, and the site's own archived red dots. |
| 2026-07-19 | [historical-globe-counter-fix](plans/2026-07-19-08-historical-globe-counter-fix.md) | E0 | done | Replaced the parked ClustrMaps service with an animated same-token historical globe; production now uses raw Busuanzi counts and local previews suppress shared localhost numbers. |
| 2026-07-19 | [alumni-globe-footer](plans/2026-07-19-07-alumni-globe-footer.md) | E0 | done | Renamed Previous to Alumni and replaced the decorative visitor card with a compact 150×150 same-token ClustrMaps globe plus preserved-map fallback. |
| 2026-07-19 | [research-directions-jss-selected](plans/2026-07-19-06-research-directions-jss-selected.md) | E0 | done | Added `[J5]`, `[J4]`, and `[C17]` to their Research Directions; promoted JSS `[J5]` to Selected Publications and synchronized its DOI/BibTeX metadata. |
| 2026-07-19 | [supervision-section](plans/2026-07-19-05-supervision-section.md) | E0 | done | Added sidebar navigation and a Supervision section with 11 Current and 5 Previous entries; shifted downstream section backgrounds to preserve alternation. |
| 2026-07-19 | [visitor-map-footer](plans/2026-07-19-03-visitor-map-footer.md) | E0 | done | Replaced the broken legacy embed with an identity-preserving live loader, a verified dated snapshot fallback, a responsive visitor card, and dependency-free Busuanzi offset logic. Summary: `docs/summaries/2026-07-19-visitor-map-footer.md`. |
| 2026-07-19 | [full-list-publication-updates](plans/2026-07-19-02-maltotal-full-publication.md) | E0 | done | Added MalTotal `[C17]`, TOSEM `[J4]`, and JSS `[J5]` to the standalone Full List with verified metadata and user-specified author annotations; no acceptance rate on `[C17]`. |
| 2026-07-19 | [pldi-2026-reviewer-award](plans/2026-07-19-01-pldi-2026-reviewer-award.md) | E0 | done | Added the PLDI 2026 reviewer award to News and Awards, pinned the SIGSOFT school funding announcement, and unpinned the ICSE 2027 News item. Official pages and HTML diff verified. |
| 2026-07-02 | [codex-ldd-guidance](plans/2026-07-02-02-codex-ldd-guidance.md) | E0 | done | Added `AGENTS.md` with Codex-facing LDD workflow, static-site structure, content conventions, and verification expectations. |
| 2026-07-02 | [scaffolding](plans/2026-07-02-01-scaffolding.md) | E0 | done | **LDD bootstrap complete.** Added `docs/PROGRESS.md` and `docs/plans/2026-07-02-01-scaffolding.md`. Project is a plain static GitHub Pages site; no build/test pipeline exists. |

## Next Steps
- **Immediate:** Monitor the published merged visitor map to confirm live green locations continue updating alongside the preserved historical dots.
- **Before any future code/content change:** Create a new dated plan under `docs/plans/` and add it to this index.
- **Likely next useful plan:** Add a lightweight static-site verification workflow for HTML/link checks and manual browser smoke testing.
- **Content update reminder:** When publications change, update both the selected and full publication lists, any linked `bibs/*.html` entry, relevant `data/` PDFs, and the news section if applicable.

## Known Issues
- The original ClustrMaps domain remains unavailable, and its raw dataset cannot be imported into MapMyVisitors. The footer performs a presentation-layer merge instead: the archived record through 23 February 2026 remains the map base, with live MapMyVisitors coordinates since 19 July 2026 overlaid in green. Provider-side counts remain separate.
- No automated validation currently exists for internal links, external links, or HTML consistency; verify manually after content updates.
- Publication metadata is duplicated across selected and full lists in `index.html`, so updates can drift unless both places are checked.

## Key Decisions
| Category | Decision |
|----------|----------|
| Build | No build system, bundler, or static site generator; preview by opening `index.html` directly. |
| Deployment | GitHub Pages deploys from the `main` branch. |
| Structure | `index.html` is the primary homepage; `stylesheet.css`, `w3.css`, `css/`, `images/`, `data/`, `bibs/`, and `html/` provide supporting styles, assets, PDFs, BibTeX snippets, and subpages. |
| Content | Follow `CLAUDE.md` conventions for news ordering, publication numbering, BibTeX files, author annotations, and service entries. |
| LDD | Keep durable project state in `docs/PROGRESS.md`; create a dated plan before future implementation or content edits. |

## Session Log

### 2026-07-19
- **Focus:** Single-map historical/live visitor merge.
- **Completed:** Replaced the interim two-card footer with one responsive map; retained the archived ClustrMaps image and historical dots as the base; registered the new MapMyVisitors widget through its public bootstrap callback; parsed public JSONP `latLng` values without evaluating provider code; projected live locations as green markers; added a compact legend, 30-second refresh, provider attribution, archive link, and historical-only failure behavior; left Busuanzi unchanged.
- **Tests:** MapMyVisitors bootstrap returned project `2248156` and valid hit IDs with both production and local referrers; its marker endpoint returned parseable coordinates; a DOM simulation verified marker placement and provider-failure fallback; exactly one merged map and one widget ID remain; no interim grid, provider-rendered map, globe, or Canvas widget remains; local homepage HTTP 200; inline JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-13-merged-visitor-map.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** Provider-side historical and live counts cannot be merged because ClustrMaps exposes no surviving raw-data export; the visible geographic record is merged on the page.

- **Focus:** Visible preservation of visitor history.
- **Completed:** Confirmed the legacy ClustrMaps token cannot be imported into MapMyVisitors; replaced the hidden historical fallback with two restrained, labelled map cards so the archived record through 23 February 2026 and live tracking since 19 July 2026 remain visible together; added a one-column mobile layout and kept Busuanzi unchanged.
- **Tests:** Legacy token returns the provider's `Error: Incorrect map code!`; archived image and live widget script both return HTTP 200; homepage returns HTTP 200 locally; no CSS rule hides the archived map; both dataset labels and tokens occur in their intended cards; inline JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-12-live-visitor-globe.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** The two providers expose no migration path for merging the legacy and replacement datasets.

- **Focus:** Final flat-map visitor presentation.
- **Completed:** Replaced the uncommitted live globe layer with the user-supplied responsive `map.js` widget; constrained it to a clean 320px maximum width; removed all globe/Canvas CSS and JavaScript; retained the dated archived map as a visual fallback and historical link; left Busuanzi counting unchanged.
- **Tests:** Valid 180×112 live tracking PNG; `map.js` and `widget_call_home.js` return valid responses; new token appears once; archived token occurs only in three fallback/history URLs; zero globe/Canvas renderer references; local homepage HTTP 200; inline JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-12-live-visitor-globe.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** None beyond the normal availability dependency on the external live-map provider.

- **Focus:** Live visitor globe restoration with the validated replacement token.
- **Completed:** Validated the replacement map token, confirmed it also supports the globe endpoint, and layered the 150px live green-marker globe over the existing archived Canvas fallback; added a separate historical-map link and retained Busuanzi counting unchanged.
- **Tests:** Valid map PNG; globe script and callback HTTP 200; callback is valid JSONP; provider includes light/dark green marker styles; new token appears once; archived token remains in four fallback/history URLs; local homepage HTTP 200; inline JavaScript syntax and `git diff --check` passed; opened local preview at the footer.
- **Files:** `index.html`, `docs/plans/2026-07-19-12-live-visitor-globe.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** None beyond the normal availability dependency on the external live-map provider.

- **Focus:** Preflight validation for a new live visitor-globe token.
- **Completed:** Confirmed the supplied widget script is reachable and contains green-marker rendering, then tested its tracking image and JSONP callback; rejected the integration before publication because the provider reports an incorrect map code. Restored the unchanged historical Canvas globe pending widget activation.
- **Tests:** Widget script HTTP 200; tracking PNG explicitly reports `Error: Incorrect map code!`; live callback returns `text/html` instead of JSONP; no new token remains in `index.html`.
- **Files:** `docs/plans/2026-07-19-12-live-visitor-globe.md`, `docs/PROGRESS.md`.
- **Blockers:** MapMyVisitors must activate or replace the supplied widget ID.

- **Focus:** Two additional supervision records.
- **Completed:** Added Thanakit Rattikanchalakorn as a current Summer Research Student and Jianing Wang as an undergraduate alumnus now pursuing a PhD at Monash.
- **Tests:** Confirmed both names occur exactly once in Supervision; Current/Alumni counts are 12/6; local homepage returned HTTP 200; inline JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-11-supervision-additions.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** Privacy-safe COMP3050 student-feedback highlights.
- **Completed:** Created a responsive summary page with four aggregate teaching indicators, the survey response rate, and paraphrased recurring positive themes; added a Teaching Experience link; kept the internal report, response count, demographics, and response-level comments out of the repository.
- **Tests:** Confirmed no COMP3050 source PDF exists in the repository; verified the four reported ratings and published 44.4% response rate; both summary and homepage returned HTTP 200; homepage inline JavaScript syntax and `git diff --check` passed; opened the summary in the local browser preview.
- **Files:** `html/comp3050-feedback-2026s1.html`, `index.html`, `docs/plans/2026-07-19-10-comp3050-feedback-summary.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** Reference-quality historical visitor globe refinement.
- **Completed:** Inspected the reference site's archived ClustrMaps renderer and confirmed its visitor coordinates were site-specific; added a local Canvas sphere renderer that crops the site's own archived visitor map, projects vertical slices with spherical curvature, rotates longitude, and applies highlight/edge shading; retained the CSS fallback, archive link, accurate count behavior, and reduced-motion mode.
- **Tests:** Local preview returned HTTP 200 and opened at the globe; confirmed Canvas surface/projection/animation primitives, zero reference-site token occurrences, only the site's own snapshot token, no dead globe script, JavaScript syntax, and `git diff --check`.
- **Files:** `index.html`, `docs/plans/2026-07-19-09-canvas-globe-refinement.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** The globe remains a clearly dated historical snapshot because the original live geolocation service is gone.

- **Focus:** Historical visitor-globe restoration and accurate page-view counting.
- **Completed:** Confirmed the ClustrMaps domain is parked; removed its dead `globe.js`; converted the verified 23 February 2026 same-token map snapshot into an animated CSS globe with its full-map link; removed the never-effective `+20000`; made Busuanzi load only on published hosts and show raw `site_pv`; replaced the shared localhost number with a preview note.
- **Tests:** Archived PNG returned HTTP 200; local preview returned HTTP 200 and opened successfully; no dead globe script, unconditional Busuanzi tag, or artificial offset remains; production-referrer Busuanzi returned HTTP 200 with a plausible raw `site_pv` (12,251 during verification); JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-08-historical-globe-counter-fix.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** Live geographic tracking is unavailable because the original third-party service is gone; the archived visitor data remains visible and the live total page-view count continues independently.

- **Focus:** Alumni terminology and compact visitor globe.
- **Completed:** Renamed the former-supervisee group to Alumni; replaced the gradient visitor card and wide snapshot with a compact 150×150 `globe.js` widget based on the supplied reference; retained the original ClustrMaps token, clickable preserved-map fallback, Busuanzi counter, and `+20000` adjustment.
- **Tests:** Local preview returned HTTP 200 and opened at the visitor footer; confirmed one Alumni heading with five entries, one globe script, no legacy live `map_v2.js`, original token preservation, JavaScript syntax, and `git diff --check`.
- **Files:** `index.html`, `docs/plans/2026-07-19-07-alumni-globe-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** Live ClustrMaps availability remains external; the compact globe fallback links to the preserved map.

- **Focus:** Research Directions and JSS selected-publication synchronization.
- **Completed:** Added JSS `[J5]` to Pointer analysis, TOSEM `[J4]` to Vulnerability detection, and ISSTA `[C17]` to Malware detection; added `[J5]` to the 2026 Selected Publications list; synchronized the full-list DOI/BIB links and replaced the preprint BibTeX with JSS volume 242, article 113027 metadata.
- **Tests:** Local preview returned HTTP 200; each new Research Directions reference and each active selected/full `[J5]` entry occurs once; DOI redirects to the correct Elsevier record; both BibTeX paths exist; JavaScript syntax and `git diff --check` passed.
- **Files:** `index.html`, `html/publications.html`, `bibs/fspta.html`, `docs/plans/2026-07-19-06-research-directions-jss-selected.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** Supervision section homepage update.
- **Completed:** Added a Supervision sidebar link and a dedicated section after Teaching; listed 11 Current and 5 Previous students with the supplied degree/institution details; shifted Tools, Education, Grants & Awards, and Misc backgrounds to preserve the alternating layout.
- **Tests:** Confirmed one navigation link and one section ID, Current/Previous counts of 11/5, every supplied name exactly once within the section, alternating section classes, JavaScript syntax, and `git diff --check`.
- **Files:** `index.html`, `docs/plans/2026-07-19-05-supervision-section.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** Visitor statistics repair and footer refresh.
- **Completed:** Preserved the existing ClustrMaps token in a non-blocking live loader; added a verified 23 February 2026 archived-map fallback, accessible availability messaging, and a responsive visitor card; changed Busuanzi to explicit HTTPS and replaced the broken jQuery-dependent `+20000` adjustment with native JavaScript.
- **Tests:** JavaScript syntax, token/endpoint checks, Wayback and Busuanzi HTTP 200 checks, responsive-rule inspection, and `git diff --check` passed. ClustrMaps itself was unreachable; Snap Firefox could not capture even `about:blank`, so browser screenshots were unavailable.
- **Files:** `index.html`, `docs/plans/2026-07-19-03-visitor-map-footer.md`, `docs/summaries/2026-07-19-visitor-map-footer.md`, `docs/PROGRESS.md`.
- **Blockers:** Live ClustrMaps availability is external; the preserved snapshot covers the visible fallback.

- **Focus:** PLDI reviewer award and SIGSOFT school funding homepage updates.
- **Completed:** Added and linked the PLDI 2026 Distinguished Artifact Evaluation Reviewer Award in News and Grants & Awards; added the SIGSOFT-supported proposal as the first pinned News item; removed the pushpin from the ICSE 2027 News item and restored it to chronological placement.
- **Tests:** Manual HTML/content inspection passed; both official pages returned successfully and contained the expected award recipient/proposal; `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-07-19-01-pldi-2026-reviewer-award.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** Full publication list updates.
- **Completed:** Added MalTotal as `[C17]` with no corresponding-author marker or acceptance rate; added the TOSEM uncertainty-estimation paper as `[J4]` with Xiao Cheng and Haoyu Wang marked as corresponding authors; added the JSS flow-sensitive pointer-analysis paper as `[J5]` with Jiahao Zhang and Xiao Cheng marked as equal contributors. Kept all three out of Selected Publications as requested.
- **Tests:** Verified the official ISSTA listing and Crossref metadata; confirmed all three identifiers occur only once and only in `html/publications.html`; checked author annotations and `git diff --check`.
- **Files:** `html/publications.html`, `docs/plans/2026-07-19-02-maltotal-full-publication.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

### 2026-07-02
- **Focus:** Codex-facing LDD initialization.
- **Completed:** Added `AGENTS.md` so future Codex sessions automatically pick up LDD workflow, repository structure, site content conventions, and verification expectations. Created and completed `docs/plans/2026-07-02-02-codex-ldd-guidance.md`.
- **Tests:** Documentation-only change; no project test suite exists.
- **Files:** `AGENTS.md`, `docs/plans/2026-07-02-02-codex-ldd-guidance.md`, `docs/PROGRESS.md`.
- **Blockers:** None.

- **Focus:** LDD bootstrap and skill repair.
- **Completed:** Repaired local `ldd` skill by replacing stale `superpowers:*` references with installed Codex companion skills and standalone fallback guidance. Bootstrapped project LDD docs with progress hub and first scaffolding plan.
- **Tests:** Verified stale `superpowers` references are gone from the local LDD skill; no project test suite exists.
- **Files:** `docs/PROGRESS.md`, `docs/plans/2026-07-02-01-scaffolding.md`, `/Users/xiao/.codex/skills/ldd/SKILL.md`.
- **Blockers:** None.
