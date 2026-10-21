# Plan: Add the ICSE 2027 Seed Patches Paper

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the user-reported ICSE 2027 acceptance, “Seed Patches to CodeQL Queries: Compositional Synthesis with Proof-of-Concept Validation”, to Selected and Full Publications as `[C21]`, with the supplied author order and contribution annotations.

**Decisions locked in:**
- Mark Weigang He and Xiao Cheng with `<sup>#</sup>` for equal contribution; bold Xiao Cheng. Mark only Shuangxiang Kan with `<sup>*</sup>` for corresponding author.
- Preserve the author order: Weigang He, Xiao Cheng, Shuangxiang Kan, Wei Li, Xingrui Yu, Ivor Tsang, Yulei Sui.
- Add a 2027 group to both publication timelines, expanded by default, following the existing Vue year-toggle pattern and ICSE badge style.
- Reuse the existing Shuangxiang Kan, Yulei Sui, and ICSE 2027 links. Follow the site's author-name-only format without affiliations or emails.
- Announce the acceptance in `10/2026` News after the pinned items. Publication metadata and acceptance are supplied by the user.
- No PDF, DOI, or BibTeX metadata was supplied; add no placeholder asset links.

## Phase 1: Content

- [x] Add matching `[C21]` entries under new 2027 groups in `index.html` and `html/publications.html`; initialize their toggle state.
- [x] Add the acceptance announcement to `index.html` News.

## Verification and Documentation

- [x] Inspect title, author order, annotations, unique IDs, year grouping, and Selected/Full consistency; check the added links and news image.
- [x] Verify the new timeline controls and run `git diff --check`.
- [x] Update `docs/PROGRESS.md` with completion, verification, changed files, next steps, and blockers; archive older records if needed.

Verification completed: identical entries and correct annotations; Vue configuration and toggle-expression checks passed; reused links returned HTTP 200; `git diff --check` passed. Independent diff review found no issues. No browser visual inspection performed.
