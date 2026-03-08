# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is **Xiao Cheng's academic homepage** (jumormt.github.io), a static GitHub Pages site. There is no build system, bundler, or static site generator — it is plain HTML/CSS/JS served directly.

## Structure

- `index.html` — The entire homepage (single-page layout with anchor-based navigation)
- `stylesheet.css` — Custom styles (fonts, links, layout)
- `w3.css` — W3.CSS framework for responsive layout and sidebar
- `css/` — Bootstrap CSS/JS
- `bibs/` — BibTeX citation snippets as standalone HTML files (e.g., `ecoop25.html`)
- `data/` — PDFs (papers, slides, CV)
- `images/` — Profile photos, icons, `new.gif` for news items
- `html/reading.html` — Curated reading list page

## Development

No build step. Open `index.html` in a browser to preview. Deploy by pushing to `main` branch (GitHub Pages).

## Content Conventions

- **News items** (in the `#news` section): Use `<li><img src="images/new.gif" alt="news">` prefix, with `MM/YYYY` date format. Newest items go first. Comment out old items with `<!-- -->` rather than deleting.
- **Publications**: Listed twice — once in "Selected Publications" and once in the expandable "Full List". Both must be updated together. Papers use `[C#]`/`[J#]`/`[P#]` numbering for conference/journal/preprint. Tags like `<span class="label label-success">CORE-A*</span>` mark venue rankings.
- **BibTeX**: Each publication's BibTeX is a separate HTML file in `bibs/` linked via `<a href="bibs/xxx.html">BIB</a>`.
- **Author annotations**: `<sup>#</sup>` = equal contribution, `<sup>*</sup>` = corresponding author. Xiao Cheng's name is always bolded with `<strong>`.
- **Services section**: TPC memberships, AE committee roles, and reviewer roles are maintained as separate `<li>` items.
- **Section alternation**: Sections alternate between default white background and `w3-light-grey` class for visual separation.
