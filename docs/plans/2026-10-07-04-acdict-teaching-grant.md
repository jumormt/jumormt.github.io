# Plan: Add the 2026 ACDICT Learning & Teaching Grant

**Epic:** E0: Site Maintenance Baseline

## Summary

Add the user's August 2026 ACDICT grant to News and Grants & Awards. Link the official scheme page and describe the project as a collaborative grant.

**Decisions locked in:**
- Use `08/2026` in News, after October and before July, retaining pinned announcements.
- Preserve the supplied project title: Teaching and Assessing Human–AI Team Competence via AI-Orchestrated Software Engineering Studios.
- News highlights selection as one of four funded projects nationally.
- Grants & Awards records AUD $9,613 as total project funding, Monash as lead institution, the four partner universities in supplied order, and Xiao Cheng and Ansgar Fehnker as Macquarie investigators.
- The official page confirms the project and four grants: https://acdict.edu.au/landt-grants/. The amount, August date, institutional roles, and Ansgar Fehnker's participation are supplied by the user (not all are listed on the official page).
- Summarize public grant details; exclude email salutation, internal funding intentions, and administrative commentary.

## Implementation

- [x] Add the `08/2026` News item to `index.html` using `images/new.gif` and the scheme URL.
- [x] Add the matching 2026 Grants & Awards item with project title, amount, and collaboration details.

## Verification and Completion

- [x] Inspect HTML, matching project titles, dates, ordering, formatting, and link destination.
- [x] Run `git diff --check` and record results in `docs/PROGRESS.md`.
- [x] Commit and push using the established session workflow.

## Verification Results

Official scheme page returned HTTP 200 and lists the project among four funded grants. Source checks confirmed two identical project titles, correct August News ordering, supplied funding amount, institution order, investigator formatting, and matching URLs. HTML diff inspected and `git diff --check` passed. No browser visual check performed.
