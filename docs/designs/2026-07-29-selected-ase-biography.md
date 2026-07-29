# Selected ASE Publications and Biography Update

## Goal

Promote the two newly accepted ASE 2026 papers from the standalone Full Publication List to the homepage Selected Publications list, and update the homepage biography to reflect both ASE coverage and first-/corresponding-author publications across ICSE, FSE, ASE, and ISSTA.

## Approved Content Design

### Selected Publications

- Add `[C18]` “RamFuzz: LLM-Guided Greybox Fuzzing for Spatial Memory Corruption via Valid Range Violation” to the top of the 2026 Selected Publications list.
- Add `[C19]` “Harnessing Uncertainty in Code Language Models: Lessons from Vulnerability Detection” immediately after `[C18]`.
- Copy titles, author orders, corresponding-author annotations, `CORE-A*`/`CCF-A` labels, and ASE research-track links from the Full Publication List.
- Use homepage-relative links and do not add unavailable PDF, slides, or BibTeX links.
- Leave the Full Publication List and News entries unchanged.

### Biography

Replace the current publication-venue sentence with:

> His papers have been published in top-tier conferences and journals in software engineering (TOSEM, ICSE, FSE, ASE, ISSTA), programming languages (OOPSLA), and security (S&P, NDSS, TDSC). Notably, he has published first- or corresponding-author papers at all four flagship software engineering conferences—ICSE, FSE, ASE, and ISSTA.

Keep the existing distinguished-paper-award clause immediately after these sentences.

## Verification

- `[C18]` and `[C19]` each appear once in Selected Publications and once in the Full Publication List.
- Both Selected entries match the corresponding Full List metadata.
- The biography names ASE and includes the approved four-conference authorship statement exactly once.
- The homepage responds successfully in a local preview.
- `git diff --check` passes.
