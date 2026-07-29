# Selected ASE Publications and Biography Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use `superpowers:executing-plans` to implement this plan task-by-task.

**Goal:** Promote `[C18]` and `[C19]` to Selected Publications, add them to the relevant Research Directions, and update the biography to include ASE and the approved first-/corresponding-author statement.

**Architecture:** This is a static-content update confined to `index.html`, with the existing Full Publication List as the metadata source of truth. The Selected entries will use homepage-relative links while the biography will preserve its existing venue-and-awards paragraph structure.

**Tech Stack:** Static HTML, Vue 2 timeline markup already present in `index.html`, LDD Markdown documentation.

**Design:** `docs/designs/2026-07-29-selected-ase-biography.md`

## Global Constraints

- Do not change the existing Full Publication List or News entries.
- Put `[C18]` first and `[C19]` second at the top of the 2026 Selected Publications list.
- Preserve the Full List titles, author orders, corresponding-author annotations, `CORE-A*`/`CCF-A` labels, and ASE research-track link.
- Do not add unavailable PDF, slides, or BibTeX links.
- Use the biography wording approved in the design document.
- Add `[C18]` to `Memory safety` and `Dynamic testing`, and add `[C19]` to `Vulnerability detection`.

---

### Task 1: Promote the ASE Papers to Selected Publications

**Files:**
- Modify: `index.html` in the 2026 Selected Publications list.

**Interfaces:**
- Consumes: `[C18]` and `[C19]` metadata from `html/publications.html`.
- Produces: Two homepage Selected Publication entries with matching metadata and homepage-relative links.

- [x] **Step 1: Record the pre-change scope check**

Run:

```bash
node -e "const s=require('fs').readFileSync('index.html','utf8'); if(s.includes('[C18]')||s.includes('[C19]')) process.exit(1)"
```

Expected: exit 0, proving neither identifier is already present on the homepage.

- [x] **Step 2: Add the two Selected Publication entries**

Insert the following at the top of the `v-show="s26"` list:

```html
<li><strong>[C18] RamFuzz: LLM-Guided Greybox Fuzzing for Spatial Memory Corruption via Valid Range Violation</strong> <span class="label label-success">CORE-A*</span> <span class="label label-success">CCF-A</span>
  <br>Shangzhi Xu, Wei Song, <a href="https://thepatrickstar.github.io/">Yuekang Li</a>, <a href="https://www.unsw.edu.au/staff/nan-sun">Nan Sun</a>, Muhammad Ejaz Ahmed, Willy Susilo, <a href="https://www.unsw.edu.au/staff/benjamin-turnbull">Benjamin Turnbull</a>, <strong>Xiao Cheng<sup>*</sup></strong>, <a href="https://siqima.me/">Siqi Ma</a><sup>*</sup>.
  <br><strong>ASE '26</strong> <a href="https://conf.researchr.org/track/ase-2026/ase-2026-research-track" class="btn btn-primary btn-xs">Page</a></li>
<li style="margin-top:8px"><strong>[C19] Harnessing Uncertainty in Code Language Models: Lessons from Vulnerability Detection</strong> <span class="label label-success">CORE-A*</span> <span class="label label-success">CCF-A</span>
  <br>Haodong Li, <strong>Xiao Cheng<sup>*</sup></strong>, Xudong Wang, Zhihao Guo, <a href="https://howiepku.github.io/">Haoyu Wang</a>.
  <br><strong>ASE '26</strong> <a href="https://conf.researchr.org/track/ase-2026/ase-2026-research-track" class="btn btn-primary btn-xs">Page</a></li>
```

- [x] **Step 3: Verify Selected/Full metadata synchronization**

Run a Node assertion that checks both identifiers occur once in `index.html` and once in `html/publications.html`, and that the title, author, label, and venue fragments match.

Expected: all assertions pass.

### Task 2: Update the Biography

**Files:**
- Modify: `index.html` in the introductory biography paragraph.

**Interfaces:**
- Consumes: The approved wording in `docs/designs/2026-07-29-selected-ase-biography.md`.
- Produces: An updated publication-venue description followed by the unchanged award clause.

- [x] **Step 1: Replace the publication-venue sentence**

Use this exact approved wording:

```html
His papers have been published in top-tier conferences and journals in software engineering (TOSEM, ICSE, FSE, ASE, ISSTA), programming languages (OOPSLA), and security (S&amp;P, NDSS, TDSC). Notably, he has published first- or corresponding-author papers at all four flagship software engineering conferences—ICSE, FSE, ASE, and ISSTA.
```

Continue with a grammatical `His work received the <b>ACM SIGSOFT Distinguished Paper Award</b>...` sentence while preserving both award names and links.

- [x] **Step 2: Verify biography wording**

Run:

```bash
rg -n "TOSEM, ICSE, FSE, ASE, ISSTA|all four flagship software engineering conferences—ICSE, FSE, ASE, and ISSTA" index.html
```

Expected: one match for each approved phrase.

### Task 3: Add the ASE Papers to Research Directions

**Files:**
- Modify: `index.html` in the Research Directions section.

**Interfaces:**
- Consumes: The new `[C18]` and `[C19]` Selected Publication entries.
- Produces: Topic references linked to the homepage Publications section.

- [x] **Step 1: Add the topic references**

Append `[<a href="#publications">C18</a>: ASE '26]` to both `Memory safety` and `Dynamic testing`. Append `[<a href="#publications">C19</a>: ASE '26]` to `Vulnerability detection`.

- [x] **Step 2: Verify the mappings**

Run a Node assertion that isolates the Research Directions section and confirms `[C18]` appears exactly twice, `[C19]` appears exactly once, and each identifier occurs in the intended topic line.

Expected: all assertions pass.

### Task 4: Verify and Complete LDD Records

**Files:**
- Modify: `docs/plans/2026-07-29-02-selected-ase-biography.md`
- Modify: `docs/PROGRESS.md`

**Interfaces:**
- Consumes: The completed homepage update and verification evidence.
- Produces: A completed LDD plan and session record.

- [x] **Step 1: Run final page and diff checks**

Run a local HTTP server and verify `/index.html` returns HTTP 200. Confirm `[C18]` and `[C19]` each occur once in Selected Publications and once in the Full List, confirm Research Directions contains the approved topic mappings, confirm the approved biography wording occurs once, and run:

```bash
git diff --check
```

Expected: local HTTP 200, all content assertions pass, and `git diff --check` exits 0.

- [x] **Step 2: Complete LDD documentation**

Mark every plan checkbox complete. Update `docs/PROGRESS.md` with status `done`, verification results, changed files, next steps, and blockers.
