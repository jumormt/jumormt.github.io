# Plan: Add NEUROSYMLAND Author Homepage Links

**Epic:** E0: Site Maintenance Baseline

## Summary

Correct the missing author homepage links in both `[C20]` entries. Prefer identifiable personal, university, or research-group profile pages and preserve all publication metadata.

## Phase 1: Verify and Add Links

- [x] Verify author identity and destination pages; document any unresolved authors.
- [x] Add matching author anchors in `index.html` and `html/publications.html`, preserving Xiao Cheng's bold text and Xi Zheng's corresponding-author marker.

## Verification and Documentation

- [x] Verify link reachability, matching entries, preserved visible text, and the HTML diff.
- [x] Run `git diff --check` and update `docs/PROGRESS.md`.
- [x] Commit and push the correction, continuing the user's publication-update push authorization.

## Verified Destinations

- Sebastian Schroder: https://researchers.mq.edu.au/en/persons/sebastian-schroder/ — Macquarie PhD profile with related autonomous-landing research and the same collaborators.
- Yao Deng: https://www.itseg.org/people/yao-deng/ — Macquarie research-group profile, autonomous-driving testing researcher.
- Jiaohong Yao: https://www.itseg.org/people/jiaohong-yao/ — Macquarie research-group profile.
- Richard Han: https://rick1han.github.io/ — personal academic homepage, Macquarie computing professor.
- Xi Zheng: https://researchers.mq.edu.au/en/persons/xi-zheng/ — existing site destination, Macquarie profile identifies Xi Zheng.

Weixian Qian and Tianyi Yang: homepage identity not yet confirmed; requested URLs from the user. Xiao Cheng retains the site's existing bold, unlinked self-name convention.

## Outcome

Added five verified coauthor links in each list (ten anchors total). All five destinations returned HTTP 200 and contained identifying text. Source checks confirm identical entries, unchanged visible text and author annotations, and no unrelated HTML changes; `git diff --check` passes. No browser visual check was performed. Weixian Qian and Tianyi Yang remain plain text pending a verified homepage or user-supplied URL; the paper identifies Tianyi Yang with UCSB, while the same-name homepage found could not be matched confidently.
