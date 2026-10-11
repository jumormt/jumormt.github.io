# Plan: Simplify the biography research introduction

**Epic:** E0: Site Maintenance Baseline

## Goal

Keep the introductory biography concise while preserving a clear technical identity in PL, SE, formal verification, and AI.

## Final scope

- Use three sentences: PL/SE/AI positioning; formal methods-based program analysis and integration of formal reasoning with AI as parallel activities; interests that extend to reliable AI infrastructure, neuro-symbolic AI, and trustworthy autonomous/embodied systems.
- Follow the latest wording preference: omit “with an emphasis on” and use “His research interests extend to”.
- Follow the user-supplied method phrasing, correcting “developes” to “develops” and using the field name “formal methods”.
- Keep the research positioning broad: omit the restrictive “verification-guided” qualifier and the introductory list of testing/repair/security tasks, following the latest user feedback.
- Per the user's clarification, retain Research Directions exactly as committed in `b31a702`.
- Preserve affiliations, honors, service, project links, publication lists, anchors, and styling.

## Tasks

- [x] Review progress, previous research/biography plans, and current text.
- [x] Simplify the biography's research introduction.
- [x] Preserve Research Directions per the user's clarification.
- [x] Inspect wording and verify that only the biography research text changed.
- [x] Update the progress log with results.

## Verification

- The HTML diff changes only the research introduction in the biography and removes the old detailed technical-method links.
- Content before and after that text, including Research Directions and publication lists, is byte-for-byte unchanged from HEAD.
- Manual wording/diff review and `git diff --check` passed. No browser visual inspection performed.
- Final wording approved by the user; commit and push to `main` authorized.
