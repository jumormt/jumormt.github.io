# Supervision Homepage Links Design

## Goal

Add reliable personal-homepage links for students listed in the homepage Supervision section, and add the user-supplied Wei Song homepage to his active RamFuzz mentions.

## Scope

- Link **Jiawei Yang** in Supervision to `https://joelyyoung.github.io/`.
- Link **Shuangxiang Kan** in Supervision to `https://shuangxiangkan.github.io/`.
- Link **Jiawei Ren** in Supervision to `https://jiawei-95.github.io/`.
- Link **Wei Song** in the July 2026 RamFuzz News item and the `[C18]` Full List author line to `https://wweisong.github.io/`.
- Preserve existing author and supervision ordering, wording, bold styling, annotations, and Current/Alumni counts.
- Leave students without a reliably verified personal homepage as plain text.
- Do not rewrite historical LDD plans or session records to retrofit links.

## Link Policy

Only personal websites or GitHub Pages sites whose contents reliably identify the intended person are eligible. LinkedIn, ResearchGate, Google Scholar, ORCID, conference profiles, and ambiguous same-name pages are excluded from this change.

## Implementation

Use ordinary `<a href="...">` links around the relevant names. In Supervision, retain each student's existing `<strong>` emphasis. No CSS or JavaScript changes are required.

## Verification

- Confirm the three Supervision links occur exactly once in the Supervision section.
- Confirm the Wei Song link appears in both active RamFuzz locations.
- Confirm all four target URLs return successfully and identify the intended people.
- Confirm Current and Alumni remain at 13 and 6 entries.
- Inspect the affected HTML and run `git diff --check`.
