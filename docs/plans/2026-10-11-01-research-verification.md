# Plan: Refresh Research Directions around verification

**Epic:** E0: Site Maintenance Baseline

## Scope

Present software verification as an established research direction and system verification for autonomous/embodied systems as the user-stated extension. Cover the recent publications already recorded on the homepage.

## Content decisions

- Use four groups: Software Verification and Static Analysis; AI for Software Engineering; Software Security and Testing; Verification and Safety of Autonomous Systems.
- Keep abstract interpretation and typestate verification together; distinguish program slicing from pointer analysis.
- Make RamFuzz, uncertainty estimation, MalTotal, and NEUROSYMLAND visible in the relevant topics.
- Place autonomous-driving scenario testing (C15) and UAV landing-site assessment (C20) under autonomous systems. Describe their actual contributions without asserting they prove system safety.
- State system-level verification for embodied intelligence as a research topic based on the user's stated direction.
- Correct J4's classification: Android malware detection/uncertainty estimation, rather than software vulnerability detection.
- Reuse existing PDFs and add precise publication anchors where no paper asset exists. Preserve publication metadata and selection.
- Leave the biography and page styling unchanged for this focused update.

## Tasks

- [x] Inspect current directions, publication records, and relevant prior plans.
- [x] Update the four research groups and paper references.
- [x] Verify local links, anchors, publication consistency, and the scoped HTML diff.
- [x] Record results and next steps in PROGRESS.md.

## Evidence

- Existing publication titles and local PDF abstracts are the evidence for paper-topic mappings.
- Abstract interpretation and verification: https://www.di.ens.fr/~cousot/AI/
- Typestate verification: https://www.microsoft.com/en-us/research/publication/typestate-verification-abstraction-techniques-complexity-results/
- Embodied AI context: https://arxiv.org/abs/2407.06886

## Verification results

- All previous research-section paper identifiers remain represented; C20 is newly included.
- All local paper files exist and have PDF signatures; all research-section anchors resolve to unique IDs.
- Research list markup is balanced, with four direction headings.
- Publication titles, author lists, annotations, selection, and other homepage sections are unchanged; publication-list edits only add anchors.
- Manually reviewed the HTML diff and inspected C5/C6/C15 PDF abstracts for topic accuracy.
- `git diff --check` passes. No browser visual inspection performed.
- No new work beyond the existing publication list was supplied during this update; future papers can be mapped into these groups.
