---
name: targeted-citation
description: >-
  Add targeted citations to manuscript text by splitting long passages into citable
  segments, searching only accepted top CS/security conference and journal venues
  (IEEE S&P, CCS, NDSS, USENIX Security, ACM CCS, etc.), filtering by publication
  time range, and exporting one reference-manager-ready output by default. Use this
  skill whenever the user asks to input text and automatically get references, add
  citations to a paragraph/manuscript, find top-venue support for statements,
  create text-to-reference correspondence, "分段引用", "自动给出引用",
  "安全会议引用", "顶会引用", "支撑文献", "补引用", "找引用", or export
  EndNote/RIS/ENW/Zotero RDF. Also trigger on general academic-writing citation
  needs even without venue-specific keywords, such as adding references while
  writing a paper, finding sources/literature for a claim, building a reference
  list, citation/referencing for academic writing, and Chinese phrasings like
  学术写作引用、写论文加引用、写paper找文献、加参考文献、配文献、引用文献、文献支撑.
version: 2.0.0
author: Yuan1z skill, refactored into static/dynamic layers
---

# Targeted Citation Search — Router

This skill is split into two layers:

- A **static layer** under `static/` that holds versioned, reusable content fragments (core principles and scope, the Chinese-user operating mode, and the citation workflow).
- A **dynamic layer** (this file plus `manifest.yaml`) that loads the core every time and reaches for heavier material only when a step needs it.

Do not try to apply the citation logic from memory or from this router. Always load fragments from disk as described below.

## Routing protocol

Follow these four steps every time the skill is invoked.

### 1. Load the manifest and the core layer

Read [manifest.yaml](manifest.yaml). Then read every file listed under `always_load`:

- `static/core/principles.md` — what the skill produces, the strict journal scope, the source hierarchy, and the search-quality rules.
- `static/core/chinese-mode.md` — how to operate when the user writes in Chinese or asks for `安全会议`/`CS顶会` style support.
- `static/core/workflow.md` — the seven-step workflow and the final report format.

### 2. No content axis — confirm scope and language inline

Unlike the other paper skills, targeted-citation has no fragment axis. Its variation is runtime parameters, not different content bodies:

- **journal scope** — `security-top4` (IEEE S&P, CCS, NDSS, USENIX Security) / `security-all` / `cs-conferences` / `custom`. Read it from the user's wording (see `core/principles.md`) and pass it to the script as `--scope`.
- **user language** — if the user writes Chinese, follow `core/chinese-mode.md` (Chinese notes, English search queries).
- **input length** — if there are more than ~10 segments, switch to the batched long-article strategy in `references/script-usage.md`.

State the detected scope and date limits in one short line before searching.

### 3. Run the workflow

Follow the seven steps in `core/workflow.md`: segment, parse, search, evaluate support conservatively, export one reference-manager file, generate review artifacts when useful, and report with the HTML browser path first. Prefer `scripts/targeted_citation.py` for the search/export when internet access is available; open `references/script-usage.md` for its full flag list and the long-article batch strategy.

Never present a paper as support merely because its title is related, and never cite a metadata-only candidate without checking the abstract or publisher page. Do not invent missing bibliographic fields.

### 4. Reach for references only when needed

The files under `references/` are deep references, not defaults. Open them on demand per the `references.on_demand` table in the manifest:

- running the script, full flags, long-article batching → `references/script-usage.md`.
- turning a claim into search queries and support grades → `references/search-strategy.md`.
- the exact CS/security venue boundary → `references/journal-scope.md`.
- RIS / EndNote / Zotero RDF export details → `references/ris-endnote.md`.

## Why this split

- The static layer is versioned and reviewable; the core stays small for a normal short run.
- The dynamic layer keeps each invocation cheap: the script flag dump and long-article strategy load only when actually running a search.
- The router itself is short on purpose. Update fragments and references, not this file, when adding scope.
- This structure mirrors `paper-writing`, `paper-polishing`, and other router-based skills.
