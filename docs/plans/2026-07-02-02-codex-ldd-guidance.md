# Plan: Codex LDD Guidance

**Epic:** E0: Site Maintenance Baseline
**Design:** N/A

## Summary

This plan completes the Codex-facing part of LDD setup by adding project instructions that future Codex sessions can read automatically. It keeps the existing static-site maintenance conventions from `CLAUDE.md` while making `docs/PROGRESS.md` the durable handoff point for all future work.

**Decisions locked in:**
- Keep existing `CLAUDE.md` unchanged for Claude-specific guidance.
- Add `AGENTS.md` for Codex-oriented project instructions.
- Do not add a build system or automated test command as part of this documentation-only setup.

---

## Phase 1: Codex Guidance

Create persistent instructions for future Codex sessions.

### [x] Task 1.1: Add project instructions
- [x] In `AGENTS.md`, document mandatory LDD session-start, planning, and session-end expectations.
- [x] In `AGENTS.md`, summarize this repository's static-site structure and content conventions.

### [x] Task 1.2: Update LDD handoff
- [x] In `docs/PROGRESS.md`, add this plan to the Plans Index.
- [x] In `docs/PROGRESS.md`, append a session log entry for the Codex guidance setup.

## Verification
- [x] `AGENTS.md` exists and references `docs/PROGRESS.md`.
- [x] `docs/plans/2026-07-02-02-codex-ldd-guidance.md` exists and is linked from the progress hub.
- [x] No project build/test command is required for this documentation-only setup.
- [x] `PROGRESS.md` updated with results.
