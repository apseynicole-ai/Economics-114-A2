# ECO114 QA Log

## 2026-06-11 - A3 past-paper and coverage audit

### What was checked

- Confirmed active branch: `feat/eco114-a3-study-hub`.
- Ran repository status and source discovery commands.
- Searched for files matching past-paper, A3, A2, framework, tutorial and unit-source naming patterns.
- Checked for local PDF text extraction tools; `pdftotext`, `pypdf`, `PyPDF2`, and `pdfplumber` were not available in the current environment.

### What was created

- Rebuilt `audit/past_paper_heatmap.md` as a source-limited A3 planning heatmap.
- Rebuilt `audit/a3_coverage_matrix.md` with unit-by-unit A3 scope, source strength, missing content and HTML destination.
- Rebuilt `sources/past_paper_index.md` with available A1/A2 past-paper-related files and a missing A3 source request.
- Rebuilt `sources/source_inventory.md` with source priority, source reliability, distribution notes and intended use.

### What was uncertain

- No clearly labelled A3 past paper, A3 memo or A3 feedback file was found.
- Exact A3 section wording, mark allocations, negative-marking rules and question-level frequencies cannot be verified until A3 source files are added.
- PDF contents were not extracted in this pass because no PDF extraction tool/library was available locally.

### Warnings

- Unit 9 remains excluded unless the lecturer later confirms it is examinable.
- A1 and A2 past-paper files are useful for format/context evidence but must not be treated as proof of A3 frequency.
- Raw university material should not be redistributed if repository visibility or sharing policy changes.
- The working tree contains unrelated pre-existing untracked/modified files that were not part of this audit.

### Next recommended step

Add the actual ECO114 A3 paper, memo and feedback files to a clearly named folder such as `sources/a3_past_papers/`, then rerun the heatmap task to extract every question by year, section, marks, unit, concept, skill and difficulty.
