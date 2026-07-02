# Plan: LDD Scaffolding

**Epic:** E0: Site Maintenance Baseline
**Design:** N/A

## Summary

This plan bootstraps Living Development Document tracking for the static academic homepage. It records the current project structure, maintenance conventions, and next-session handoff points so future updates can start from durable repository context instead of chat history.

**Decisions locked in:**
- The site remains a plain static GitHub Pages repository with no build pipeline.
- LDD files live under `docs/` and should be updated before ending future sessions.
- `CLAUDE.md` remains the source for site-specific content conventions.

---

## Phase 1: Repository Context

Capture the current project shape and existing maintenance constraints.

### [x] Task 1.1: Inspect project documentation
- [x] Read `README.md`.
- [x] Read `CLAUDE.md`.
- [x] Review recent git history for current maintenance patterns.

### [x] Task 1.2: Inspect static-site structure
- [x] Identify primary files and folders: `index.html`, `stylesheet.css`, `w3.css`, `css/`, `bibs/`, `data/`, `html/`, and `images/`.
- [x] Confirm there is no build system or package manifest.

## Phase 2: LDD Bootstrap

Create the durable LDD state files for future sessions.

### [x] Task 2.1: Create progress hub
- [x] Add `docs/PROGRESS.md`.
- [x] Record current epic, plans index, next steps, known issues, key decisions, and session log.

### [x] Task 2.2: Create first plan
- [x] Add `docs/plans/2026-07-02-01-scaffolding.md`.
- [x] Mark completed bootstrap tasks and record verification expectations.

## Verification
- [x] `docs/PROGRESS.md` exists and reflects the repository state.
- [x] `docs/plans/2026-07-02-01-scaffolding.md` exists and is linked from the progress hub.
- [x] No project build/test command is required for this documentation-only bootstrap.
- [x] PROGRESS.md updated with results.
