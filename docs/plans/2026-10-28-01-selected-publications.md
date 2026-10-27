# Plan: Add DeepWukong, TDSC, and RamFuzz to Selected Publications

- **Date:** 2026-10-28
- **Status:** done (content and verification; commit/push authorized)
- **Task:** Add existing Full List entries `[J1]`, `[J2]`, and `[C18]` to the homepage Selected Publications, then commit and push to `main` as requested.

## Tasks

- [x] Read project progress and relevant publication design/history; identify source entries.
- [x] Copy the three entries with homepage-relative links into their existing year groups; expand the 2020 heading to 2020 - 2021.
- [x] Verify metadata equality, chronology, local PDF/BibTeX links, and HTML diff.
- [x] Update the progress log and prepare only task changes for the authorized commit/push to origin/main.

## Scope

Preserve Full List metadata and all other selected papers. Keep author links, bolding, annotations, and badges consistent with the source entries. Preserve unrelated local work without including it in this commit.

## Verification and Delivery

- Selected/Full entries match after normalizing whitespace, list-item attributes, and relative link prefixes; titles, authors, annotations, badges, and links are preserved.
- Each requested paper appears once in its expected existing year group; existing selected entries and unrelated homepage content are preserved.
- Linked local PDFs have valid PDF headers; BibTeX targets exist and metadata was inspected. ASE Page returned HTTP 200.
- Unique IDs, balanced publication list items, and `git diff --check` passed; no browser visual inspection performed.
- Fast-forwarded six upstream commits from `9b076bb` to `52cc136`, preserving ICSE 2027 updates and unrelated local work.
- User explicitly requested commit/push to `main`; GitHub Pages deploys from that branch.
