# jumormt.github.io Development Progress

## Current Epic
**E0: Site Maintenance Baseline** — Maintain Xiao Cheng's static academic homepage with reliable cross-session documentation for content, publication, service, and asset updates.

## Epics
- [x] E0: Site Maintenance Baseline
- [ ] E1: Future content updates and site improvements

## Plans Index (active/recent — see `SESSION-LOG-ARCHIVE.md` for earlier plans)
| Date | Plan | Epic | Status | Notes |
|------|------|------|--------|-------|
| 2026-10-21 | [icse-2027-direct-acceptance](plans/2026-10-21-04-icse-2027-direct-acceptance.md) | E0 | done | Added Direct Accept badges and 119/2375=5.01% direct acceptance rates to all three entries; updated both News items. |
| 2026-10-21 | [icse-2027-membership-inference](plans/2026-10-21-03-icse-2027-membership-inference.md) | E0 | done | Added `[C22]` to Full Publications and News only, with Xiao Cheng as an ordinary coauthor; local preview verified. |
| 2026-10-21 | [seed-patches-author-links](plans/2026-10-21-02-seed-patches-author-links.md) | E0 | done | Added verified Xingrui Yu personal and Ivor Tsang A*STAR profile links to both `[C21]` entries and News; local preview updated. |
| 2026-10-21 | [icse-2027-seed-patches](plans/2026-10-21-01-icse-2027-seed-patches.md) | E0 | done | Added `[C21]` to both 2027 lists and News; Weigang He/Xiao Cheng share equal-contribution marks, Shuangxiang Kan is corresponding author. |
| 2026-10-11 | [static-analysis-heading](plans/2026-10-11-04-static-analysis-heading.md) | E0 | done | Renamed the heading to Static Analysis and Software Verification. |
| 2026-10-11 | [autonomous-research-scope](plans/2026-10-11-03-autonomous-research-scope.md) | E0 | done | Removed the research summary; broadened C15/C20 topics to safety testing and neuro-symbolic reasoning for autonomous systems. |
| 2026-10-11 | [research-overview-simplification](plans/2026-10-11-02-research-overview-simplification.md) | E0 | done | Refined the biography around formal methods, integration of formal reasoning and AI, and broad AI infrastructure/neuro-symbolic/autonomous-system interests; retained Research Directions. |
| 2026-10-11 | [research-verification](plans/2026-10-11-01-research-verification.md) | E0 | done | Added explicit software/system verification directions, C20, refined recent-paper mappings, and direct paper anchors. |
| 2026-10-07 | [majordomo-catalyst-grant](plans/2026-10-07-05-majordomo-catalyst-grant.md) | E0 | done | Added MajorDomo Catalyst Grant to Grants & Awards only with four team members and user-confirmed 2026 year; actual funding amount not yet supplied. |
| 2026-10-07 | [acdict-teaching-grant](plans/2026-10-07-04-acdict-teaching-grant.md) | E0 | done | Added the August ACDICT grant to News and Grants & Awards with project title, AUD $9,613 total funding, four-university collaboration, and official scheme link. |
| 2026-10-07 | [neurosymland-author-links](plans/2026-10-07-03-neurosymland-author-links.md) | E0 | done | Added five verified coauthor links to each `[C20]` entry; Weixian Qian and Tianyi Yang remain unlinked pending verified URLs. |
| 2026-10-07 | [ase-reviewer-award](plans/2026-10-07-02-ase-reviewer-award.md) | E0 | done | Added matching ASE 2026 Distinguished Reviewer Award entries to News (`10/2026`) and Grants & Awards. |
| 2026-10-07 | [neurosymland-publication](plans/2026-10-07-01-neurosymland-publication.md) | E0 | done | Added matching IROS 2026 `[C20]` entries to Selected and Full Publications with CORE-A and Best Paper Candidate badges. |

## Next Steps
- **Publication follow-up:** ICSE 2027 `[C21]` and `[C22]` are complete; `[C22]` is Full-List-only per user preference. Add PDF/DOI/BibTeX links when supplied.
- **Immediate:** MajorDomo Catalyst Grant year confirmed as 2026 and updated. Add its actual funding amount only when confirmed by the award notification.
- **Pending links:** Add Weixian Qian and Tianyi Yang homepage URLs if supplied or reliably identified.
- **Before any future code/content change:** Create a new dated plan under `docs/plans/` and add it to this index.
- **Likely next useful plan:** Add a lightweight static-site verification workflow for HTML/link checks and manual browser smoke testing.
- **Content update reminder:** When publications change, update both the selected and full publication lists, any linked `bibs/*.html` entry, relevant `data/` PDFs, and the news section if applicable.

## Known Issues
- No automated validation currently exists for internal links, external links, or HTML consistency; verify manually after content updates.
- Publication metadata is duplicated across `index.html` and `html/publications.html`, so updates can drift unless both places are checked.

## Key Decisions
| Category | Decision |
|----------|----------|
| Build | No build system, bundler, or static site generator; preview by opening `index.html` directly. |
| Deployment | GitHub Pages deploys from the `main` branch. |
| Structure | `index.html` is the primary homepage; `stylesheet.css`, `w3.css`, `css/`, `images/`, `data/`, `bibs/`, and `html/` provide supporting styles, assets, PDFs, BibTeX snippets, and subpages. |
| Content | Follow `CLAUDE.md` conventions for news ordering, publication numbering, BibTeX files, author annotations, and service entries. |
| LDD | Keep durable project state in `docs/PROGRESS.md`; create a dated plan before future implementation or content edits. |

## Session Log

### 2026-10-21
- **Focus:** Annotate both ICSE 2027 papers as direct acceptances.
- **Completed:** Added `Direct Accept` badges and `direct acceptance rate: 119/2375=5.01%` to `[C21]` in Selected/Full and `[C22]` in Full only; updated both News items to “directly accepted”.
- **Verification:** Decimal calculation, exact three-entry/two-news counts, matching C21 metadata, unchanged author roles/selection, and exact unrelated-HTML preservation passed. Independent review and `git diff --check` passed; fetched remote `main` has no divergence. No browser visual inspection performed; links/assets unchanged.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-21-04-icse-2027-direct-acceptance.md`, `docs/PROGRESS.md`.
- **Next steps:** Continue the user's commit/push authorization for this follow-up; publication PDF/DOI/BibTeX links remain pending supply.
- **Blockers:** None; direct acceptance outcome and 119/2375 counts are user-supplied.

- **Focus:** Publish the approved ICSE 2027 updates.
- **Completed:** Following the user's explicit “commit push” request, pushed the three content commits (`4647e23`, `cb55e87`, `f055c86`) to `origin/main`; remote advanced from `9b076bb` to `f055c86`.
- **Verification:** Fetched remote `main` and confirmed no divergence (three local commits ahead); previous content/link checks and independent reviews passed; `git diff --check` passed; `git push origin main` succeeded.
- **Files:** The published content/docs from the three October 21 plans, plus this session record. The pre-existing untracked `.claude/` directory was not included.
- **Next steps:** GitHub Pages deployment follows the push; add publication PDF/DOI/BibTeX links when supplied.
- **Blockers:** None.

- **Focus:** Add the ICSE 2027 Membership or Predictability paper.
- **Completed:** Added `[C22]` to Full Publications under 2027 and an acceptance announcement to `10/2026` News. Preserved the supplied four-author order and bolded Xiao Cheng without contribution-role superscripts; Selected Publications is unchanged as requested.
- **Verification:** Checked exact title/author order, unique numbering, ordinary-coauthor formatting, preserved prior entries and Selected content, news date and links. Both reused URLs returned HTTP 200. Restarted the stopped local preview and verified both served pages match source; independent review and `git diff --check` passed. No browser visual inspection performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-21-03-icse-2027-membership-inference.md`, `docs/PROGRESS.md`.
- **Next steps:** Review at `http://127.0.0.1:8000/html/publications.html#pub-c22`; add asset links when supplied. No remote push/deployment performed.
- **Blockers:** None. ICSE 2027 follows the ongoing acceptance-update context; title, author order, and participation role are user-supplied.

- **Focus:** Add Xingrui Yu and Ivor Tsang author homepage links.
- **Completed:** Added both verified destinations to `[C21]` in Selected/Full Publications and its acceptance News, preserving all visible text and author annotations.
- **Verification:** Both URLs returned HTTP 200 and identifying affiliation/email evidence. Confirmed six new anchors, identical publication entries, and byte-for-byte original HTML after removing only those anchors. Both local preview pages serve updated content; `git diff --check` passed. No browser visual inspection performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-21-02-seed-patches-author-links.md`, `docs/PROGRESS.md`.
- **Next steps:** User can refresh the local preview at `http://127.0.0.1:8000/#pub-c21`; no push/deployment performed.
- **Blockers:** None.

- **Focus:** Add the user-reported ICSE 2027 Seed Patches acceptance.
- **Completed:** Added identical `[C21]` entries under new expanded 2027 groups in Selected and Full Publications, with the supplied seven-author order, equal-contribution marks for Weigang He/Xiao Cheng, and a corresponding-author mark for Shuangxiang Kan; added `10/2026` News. Archived older plan-index rows and session logs without deleting history.
- **Verification:** Manual diff and independent review passed; checked exact metadata, annotation counts, unique IDs, preserved prior publication numbers, and Selected/Full equality. Vue configuration/default state/toggle expressions passed; all three reused URLs returned HTTP 200; news image exists; `git diff --check` passed. No browser visual inspection performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-21-01-icse-2027-seed-patches.md`, `docs/PROGRESS.md`, `docs/plans/SESSION-LOG-ARCHIVE.md`.
- **Next steps:** No remaining content edits; add publication asset links when supplied. No push/deployment performed in this session.
- **Blockers:** None; acceptance and author roles supplied by the user.

### 2026-10-11
- **Focus:** Research heading order.
- **Completed:** Renamed the first direction to “Static Analysis and Software Verification”.
- **Verification:** One-line HTML diff inspected; `git diff --check` passed; all topic entries and links unchanged.
- **Files:** `index.html`, `docs/plans/2026-10-11-04-static-analysis-heading.md`, `docs/PROGRESS.md`.
- **Next steps:** User authorized commit and push to `main`; no remaining content edits.
- **Blockers:** None.

- **Focus:** Broaden autonomous-systems topics in Research Directions.
- **Completed:** Removed the redundant opening sentence and replaced the specific scenario-generation and UAV landing-site labels with “Safety testing of autonomous systems” and “Neuro-symbolic reasoning for autonomous systems”. Retained the heading, embodied verification topic, and paper references.
- **Verification:** Manual diff/exact comparison confirms only the requested text changed; all links unchanged; C15 PDF and C20 anchor verified; `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-10-11-03-autonomous-research-scope.md`, `docs/PROGRESS.md`.
- **Next steps:** User authorized commit and push to `main`; no remaining content edits.
- **Blockers:** None.

- **Focus:** Finalize the introductory research biography.
- **Completed:** User approved the three-sentence biography: PL/SE/AI positioning, formal methods-based program analysis and integration of formal reasoning with AI, and interests extending to reliable AI infrastructure, neuro-symbolic AI, and trustworthy autonomous/embodied systems. Research Directions is unchanged. Intermediate revisions are preserved in the session archive.
- **Verification:** Reviewed the final HTML diff; byte comparison confirms changes are confined to the biography research text; `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-10-11-02-research-overview-simplification.md`, `docs/plans/SESSION-LOG-ARCHIVE.md`, `docs/PROGRESS.md`.
- **Next steps:** User authorized commit and push to `main`; no remaining content edits.
- **Blockers:** None.

- **Focus:** Research Directions update for software and autonomous-system verification.
- **Completed:** Reorganized into four groups; highlighted abstract interpretation and typestate verification; added the user-stated embodied-system verification topic and NEUROSYMLAND; moved autonomous-driving testing into the systems group; clarified RamFuzz, uncertainty estimation, program slicing, and MalTotal mappings; corrected J4's malware classification and added precise publication anchors.
- **Verification:** All previous paper references retained; local PDFs and anchors valid; unique IDs and balanced research lists; publication metadata/selection and unrelated homepage content unchanged; manual HTML/PDF abstract review and `git diff --check` passed. No browser visual inspection performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-11-01-research-verification.md`, `docs/PROGRESS.md`.
- **Next steps:** User approved commit and push to `main`; map additional system-verification projects when supplied.
- **Blockers:** None.

- **Focus:** Pull remote main while preserving local work.
- **Completed:** Fast-forwarded 18 commits from `1d0407e` to `62a9249`; resolved the autostash conflict caused by upstream log archival while retaining the local skill-migration plan entry and session record. Existing untracked files remain in place.
- **Verification:** Checked branch synchronization, preservation of local additions, absence of unmerged paths, and `git diff --check`.
- **Files:** `docs/PROGRESS.md` (local reconciliation and session log); remote changes supplied by the pull.
- **Next steps:** No further pull work; existing content follow-ups above remain pending.
- **Blockers:** None.

### 2026-10-07
- **Focus:** Confirm MajorDomo grant year and investigate funding amount.
- **Completed:** Added `2026` to the existing Awards entry after the user confirmed today's notification. Found an official 2025 Catalyst award of AUD $25,000, but no confirmed allocation for this MajorDomo project; left its amount unspecified.
- **Verification:** Confirmed the year prefix is the only HTML change and News is unchanged; `git diff --check` passed.
- **Files:** `index.html`, `docs/plans/2026-10-07-05-majordomo-catalyst-grant.md`, `docs/PROGRESS.md`.
- **Remaining:** Actual MajorDomo funding amount requires the award notification or approved budget; public precedent is not project-specific confirmation.

- **Focus:** Add the Macquarie University MajorDomo Catalyst Grant.
- **Completed:** Added an Awards-only internal teaching grant entry with the full project title, Ansgar Fehnker as primary contact, and Nader Hanna, Xiao Cheng, and Gunjan Chamania with their affiliations. Kept News and the existing 2025 grant unchanged.
- **Verification:** Confirmed one exact-title entry, all four members in supplied order, role/affiliation formatting, bold Xiao Cheng, and unchanged prior HTML after removing the added line; `git diff --check` passes. No links/assets added or browser visual check performed.
- **Files:** `index.html`, `docs/plans/2026-10-07-05-majordomo-catalyst-grant.md`, `docs/PROGRESS.md`.
- **Remaining:** Award year was not supplied and remains omitted pending the requested clarification. No blocker for the published grant details.

- **Focus:** Add the August 2026 ACDICT Learning & Teaching grant.
- **Completed:** Added News (`08/2026`) and Grants & Awards entries with the project title, selection among four funded projects, official scheme link, AUD $9,613 total funding, four institutions, Monash project lead, and Macquarie investigators Xiao Cheng and Ansgar Fehnker.
- **Verification:** Official URL returned HTTP 200 and confirmed the project and four grants; checked title consistency, News chronology, amount, investigator formatting, institution order, and HTML diff; `git diff --check` passed. No browser visual check performed.
- **Files:** `index.html`, `docs/plans/2026-10-07-04-acdict-teaching-grant.md`, `docs/PROGRESS.md`.
- **Blockers:** None. August date, amount, institutional roles, and Ansgar Fehnker's participation come from the user's supplied project details.

- **Focus:** Correct missing NEUROSYMLAND author homepage links.
- **Completed:** Added Sebastian Schroder, Yao Deng, Jiaohong Yao, Richard Han, and Xi Zheng links to both `[C20]` entries; retained author order, Xiao Cheng bolding, corresponding-author annotation, and all other publication metadata. Continued the user's commit/push workflow.
- **Verification:** All five target URLs returned HTTP 200 and identifying text; both entries are identical, with five anchors each; visible text and unrelated HTML are unchanged; `git diff --check` passes. No browser visual check performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-07-03-neurosymland-author-links.md`, `docs/PROGRESS.md`.
- **Remaining:** Weixian Qian and Tianyi Yang remain plain text because their homepages could not be confidently identified; asked the user for URLs. Verified links are documented in the plan.

- **Focus:** Add the user-reported ASE 2026 Distinguished Reviewer Award.
- **Completed:** Added a `10/2026` News announcement after pinned items and a separate 2026 Grants & Awards entry, using the exact supplied award name.
- **Verification:** Inspected HTML diff; confirmed one matching entry in each section, correct ordering/date, existing news image, and passing `git diff --check`. No new links; no browser visual check performed.
- **Files:** `index.html`, `docs/plans/2026-10-07-02-ase-reviewer-award.md`, `docs/PROGRESS.md`.
- **Blockers:** None. Award information supplied by the user; News uses the current announcement month.

- **Focus:** Add the user-supplied NEUROSYMLAND IROS 2026 paper.
- **Completed:** Added `[C20]` at the top of both 2026 lists with CORE-A and Best Paper Candidate badges; preserved author order, bolded Xiao Cheng, and marked Xi Zheng as corresponding author. Normalized Sebastian Schroder's capitalization. Archived older session logs without deleting history.
- **Verification:** Inspected the HTML diff; confirmed exactly one active `[C20]` per page and identical entries after whitespace normalization; `git diff --check` passed. No new links or assets. No browser visual check performed.
- **Files:** `index.html`, `html/publications.html`, `docs/plans/2026-10-07-01-neurosymland-publication.md`, `docs/PROGRESS.md`, `docs/plans/SESSION-LOG-ARCHIVE.md`.
- **Blockers:** None. Publication metadata and candidate status come from the user; no PDF, DOI, or BibTeX link was supplied.

Older plans and sessions through 2026-08-28: see [Session Log Archive](plans/SESSION-LOG-ARCHIVE.md).
