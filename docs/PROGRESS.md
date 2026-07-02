# jumormt.github.io Development Progress

## Current Epic
**E0: Site Maintenance Baseline** — Maintain Xiao Cheng's static academic homepage with reliable cross-session documentation for content, publication, service, and asset updates.

## Epics
- [x] E0: Site Maintenance Baseline
- [ ] E1: Future content updates and site improvements

## Plans Index (active/recent — see `SESSION-LOG-ARCHIVE.md` for earlier plans)
| Date | Plan | Epic | Status | Notes |
|------|------|------|--------|-------|
| 2026-07-02 | [codex-ldd-guidance](plans/2026-07-02-02-codex-ldd-guidance.md) | E0 | done | Added `AGENTS.md` with Codex-facing LDD workflow, static-site structure, content conventions, and verification expectations. |
| 2026-07-02 | [scaffolding](plans/2026-07-02-01-scaffolding.md) | E0 | done | **LDD bootstrap complete.** Added `docs/PROGRESS.md` and `docs/plans/2026-07-02-01-scaffolding.md`. Project is a plain static GitHub Pages site; no build/test pipeline exists. |

## Next Steps
- **Before any future code/content change:** Create a new dated plan under `docs/plans/` and add it to this index.
- **Likely next useful plan:** Add a lightweight static-site verification workflow for HTML/link checks and manual browser smoke testing.
- **Content update reminder:** When publications change, update both the selected and full publication lists, any linked `bibs/*.html` entry, relevant `data/` PDFs, and the news section if applicable.

## Known Issues
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
