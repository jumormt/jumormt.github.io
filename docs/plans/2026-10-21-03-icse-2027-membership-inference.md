# Plan: Add the ICSE 2027 Membership Inference Paper

**Epic:** E0: Site Maintenance Baseline

## Summary

Add “Membership or Predictability? Characterizing Member-Likeness through Representation Engineering for Code LLM Membership Inference” as `[C22]` in the Full Publications 2027 group and announce its acceptance in News. The user's “also accepted” refers to ICSE 2027 in the ongoing conversation.

**Decisions locked in:**
- Follow the user's explicit Full-List-only scope; leave Selected Publications unchanged.
- Preserve the supplied author order: Hongzhou Rao, Haodong Li, Xiao Cheng, Haoyu Wang. Bold Xiao Cheng as an ordinary coauthor, without equal-contribution or corresponding-author marks. No other contribution roles were supplied.
- Reuse the existing Haoyu Wang and ICSE 2027 links and ICSE ranking badges; use the site's name-only format without affiliations or emails.
- Add `[C22]` above `[C21]` in the Full List and use `10/2026` for the acceptance news, after pinned items.
- No PDF, DOI, BibTeX, or acceptance-rate details were supplied; do not add placeholders.
- Keep local preview available; no remote push is requested.

## Content and Verification

- [x] Add `[C22]` to `html/publications.html` and its acceptance news to `index.html`.
- [x] Verify exact title/author order, Xiao Cheng's bolding without role annotations, unique numbering, year grouping, unchanged Selected Publications, and preserved `[C21]`.
- [x] Check reused links, local preview content, and `git diff --check`; obtain independent diff review.
- [x] Update `docs/PROGRESS.md` with outcome, verification, files, next steps, and blockers.

## Outcome

Added `[C22]` only to Full Publications, plus a `10/2026` acceptance news item. Exact title, supplied author order, ordinary-coauthor formatting, numbering, year group, unchanged Selected section, and preserved prior entries were verified. Both reused URLs returned HTTP 200. The local preview had stopped; restarted it on port 8000 and verified both served pages match their updated source. Independent review found no issues; `git diff --check` passed. No browser visual inspection performed; no remote push/deployment.
