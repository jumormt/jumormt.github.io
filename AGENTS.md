# Repository Instructions

This repository is `jumormt.github.io`, a plain static GitHub Pages site for Xiao Cheng's academic homepage. There is no build system, bundler, package manager, or static-site generator.

## LDD Workflow

This project uses LDD (Living Development Document) for cross-session continuity. Durable state lives in `docs/`.

Before starting development or content changes:

1. Read `docs/PROGRESS.md` in full.
2. Check the Plans Index and read any plan named in Next Steps when relevant.
3. If related `docs/FUTURE.md`, `docs/summaries/`, `docs/designs/`, `docs/bugs/`, or `docs/debug/` files exist for the task, read the relevant ones.
4. State what plan or task is being resumed before changing files.

For new work:

1. Create a dated plan under `docs/plans/YYYY-MM-DD-NN-<topic>.md` before editing implementation or content files.
2. Add the plan to `docs/PROGRESS.md`.
3. Work through the plan and mark tasks complete as they are finished.
4. End every session by updating `docs/PROGRESS.md` with status, next steps, tests or verification, changed files, and blockers.

Keep `docs/PROGRESS.md` concise. Archive old session logs or completed plans into `docs/plans/SESSION-LOG-ARCHIVE.md` instead of deleting history.

## Site Structure

- `index.html` is the primary homepage and single-page layout.
- `stylesheet.css`, `w3.css`, and `css/` provide styles and legacy dependencies.
- `bibs/` contains BibTeX citation snippets as standalone HTML files.
- `data/` contains PDFs such as papers, slides, and CV files.
- `images/` contains profile images, icons, and `new.gif`.
- `html/` contains supporting pages such as the reading list and research pages.

Preview by opening `index.html` directly in a browser. Deployment happens through GitHub Pages from the `main` branch.

## Content Conventions

- News entries in `#news` use `MM/YYYY` dates, newest first, and the `images/new.gif` prefix for new items.
- Old news is commented out instead of deleted when preserving history is useful.
- Publications appear in both selected and full lists; update both places together.
- Publication numbering uses `[C#]`, `[J#]`, and `[P#]` for conference, journal, and preprint entries.
- BibTeX links point to matching files under `bibs/`.
- Xiao Cheng's name should be bolded with `<strong>`.
- Author annotations use `<sup>#</sup>` for equal contribution and `<sup>*</sup>` for corresponding author.
- Service entries are maintained as separate list items.
- Sections alternate default white and `w3-light-grey` backgrounds.

## Verification

There is currently no automated test suite. For content edits, inspect affected HTML manually and verify links, anchors, PDFs, BibTeX snippets, and duplicated publication entries.
