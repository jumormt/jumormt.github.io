# Supervision Homepage Links Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add verified personal-homepage links for three supervised students and Wei Song without changing names, ordering, annotations, or supervision counts.

**Architecture:** This is a static-content-only change. Add ordinary anchors to the relevant names in `index.html` and `html/publications.html`; retain the existing `<strong>` styling in Supervision and leave all unverified student names as plain text.

**Tech Stack:** Plain HTML, shell-based static checks, local HTTP preview

**Epic:** E0: Site Maintenance Baseline
**Design:** `docs/superpowers/specs/2026-08-28-supervision-homepage-links-design.md`

## Global Constraints

- Only link Jiawei Yang, Shuangxiang Kan, and Jiawei Ren in Supervision.
- Link Wei Song only in the active July 2026 RamFuzz News item and `[C18]` Full List author line.
- Preserve all author and supervision ordering, wording, bold styling, annotations, and Current/Alumni counts.
- Do not add LinkedIn, ResearchGate, Google Scholar, ORCID, conference-profile, or ambiguous same-name links.
- Do not retrofit links into historical LDD documents.

---

### Task 1: Add the verified links

**Files:**
- Modify: `index.html:271`
- Modify: `index.html:460`
- Modify: `index.html:471-472`
- Modify: `html/publications.html:45`

**Interfaces:**
- Consumes: The approved URL/name mappings in the design document.
- Produces: Static anchors rendered by the existing homepage and Full List pages; no JavaScript or CSS interface changes.

- [x] **Step 1: Run pre-change checks to prove the target links are absent**

```bash
rg -n '<strong><a href="https://(joelyyoung|shuangxiangkan|jiawei-95)\.github\.io/">' index.html
rg -n '<a href="https://wweisong\.github\.io/">Wei Song</a>' index.html html/publications.html
```

Expected: both commands return no matches and exit with status 1.

- [x] **Step 2: Add the three Supervision anchors in `index.html`**

Use this exact name markup while leaving the surrounding degree/status text unchanged:

```html
<strong><a href="https://joelyyoung.github.io/">Jiawei Yang</a></strong>
<strong><a href="https://shuangxiangkan.github.io/">Shuangxiang Kan</a></strong>
<strong><a href="https://jiawei-95.github.io/">Jiawei Ren</a></strong>
```

- [x] **Step 3: Add the Wei Song anchors**

Replace the plain-text name with the following markup in the July 2026 RamFuzz News item in `index.html` and the `[C18]` author line in `html/publications.html`:

```html
<a href="https://wweisong.github.io/">Wei Song</a>
```

- [x] **Step 4: Run focused post-change checks**

```bash
rg -n '<strong><a href="https://(joelyyoung|shuangxiangkan|jiawei-95)\.github\.io/">[^<]+</a></strong>' index.html
rg -n '<a href="https://wweisong\.github\.io/">Wei Song</a>' index.html html/publications.html
```

Expected: the first command reports exactly three Supervision entries; the second reports exactly two RamFuzz entries, one in each file.

- [x] **Step 5: Commit the static HTML change**

```bash
git add index.html html/publications.html
git commit -m "Link supervision and RamFuzz author homepages"
```

### Task 2: Verify rendering, URLs, and preserved structure

**Files:**
- Modify: `docs/plans/2026-08-28-01-supervision-homepage-links.md`
- Modify: `docs/PROGRESS.md`

**Interfaces:**
- Consumes: The HTML produced by Task 1.
- Produces: A completed LDD record containing verification results and the final changed-file list.

- [x] **Step 1: Verify all target pages are reachable**

```bash
for url in https://joelyyoung.github.io/ https://shuangxiangkan.github.io/ https://jiawei-95.github.io/ https://wweisong.github.io/; do curl -LIsS --max-time 20 "$url" | head -n 1; done
```

Expected: four successful HTTP status lines (`200` after redirect handling, or an initial redirect followed by successful content retrieval).

- [x] **Step 2: Verify the Supervision counts and list-item totals are unchanged**

```bash
rg -n 'Current <span class="supervision-group-count">\(13\)</span>|Alumni <span class="supervision-group-count">\(6\)</span>' index.html
sed -n '448,476p' index.html | rg -c '<li>'
```

Expected: both displayed counts are present and the section contains `19` list items.

- [x] **Step 3: Preview both affected pages locally**

```bash
python3 -m http.server 8000
```

Expected: `http://127.0.0.1:8000/index.html#supervision` and `http://127.0.0.1:8000/html/publications.html` return HTTP 200; manual inspection shows linked bold student names and a linked Wei Song name with no layout regression.

Verification note: both pages returned HTTP 200 and their served HTML contained all five intended anchors. No browser session was available for screenshot-based visual inspection, so the local served output and unchanged inline-only markup were inspected instead.

- [x] **Step 4: Run final static checks**

```bash
git diff --check
git diff -- index.html html/publications.html
```

Expected: `git diff --check` is silent, and the HTML diff contains only the five intended anchor insertions.

- [x] **Step 5: Complete the LDD records**

Mark every plan checkbox complete. Set this plan to `done` in `docs/PROGRESS.md`, restore the default future-maintenance Next Steps, and add a 2026-08-28 Session Log entry recording completed work, verification, changed files, and blockers.

- [x] **Step 6: Commit the completed LDD records**

```bash
git add docs/plans/2026-08-28-01-supervision-homepage-links.md docs/PROGRESS.md
git commit -m "Record homepage link update"
```

## Verification

- [x] Three verified student homepage links occur in Supervision.
- [x] The Wei Song homepage link occurs in both active RamFuzz locations.
- [x] All four external targets return successfully and identify the intended people.
- [x] Current and Alumni remain at 13 and 6 entries, respectively.
- [x] Both affected pages return HTTP 200 in a local preview.
- [x] Manual HTML inspection passes via served-output and source-diff inspection; no browser session was available.
- [x] `git diff --check` passes.
- [x] `docs/PROGRESS.md` records the final result.
