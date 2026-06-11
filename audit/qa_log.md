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

## 2026-06-11 - A3 individual PDF source import and real heatmap

### What was checked

- Confirmed branch `feat/eco114-a3-study-hub`.
- Located the cleaner A3 source PDFs in `/Users/nicole/Downloads`.
- Copied A3 papers, memos, feedback files and support guides into `sources/raw/`.
- Confirmed the combined DOCX extraction at `sources/extracted/ECO_A3_PAST_PAPERS_extracted.txt` is readable and contains 2024, 2023 and 2022 A3 papers.

### Extraction method

- `textutil` successfully extracted the combined DOCX source to plain text.
- `textutil` was tested on individual PDFs but produced PDF object streams rather than usable text. The PDFs are preserved as raw authoritative sources, while the readable DOCX extraction supplies the question text for the heatmap.

### What was created

- Replaced the preliminary missing-source heatmap with a real question-level heatmap covering 169 extracted rows from 2022, 2023 and 2024 A3 papers.
- Updated the A3 coverage matrix with real unit counts and visible marks.
- Updated the past-paper index and source inventory with the new raw PDF source set.

### Uncertainties

- The 2025 Afrikaans A3 assessment and 2025 Section C feedback are present but not question-extracted because local PDF extraction was not readable.
- Some graph labels from embedded figures are necessarily summarised rather than transcribed in full because extracted text does not preserve images/diagrams.

### Next recommended task

Build the A3 exam warroom first: formula bank, T/F danger bank, MCQ trap bank, graph redraw bank, and Section C answer templates based directly on this heatmap.

## 2026-06-11 - Markets hub v1 content build

### What was built

- Replaced the scaffold in `exports/html/eco114_a3_markets_units_6_7_8_10.html` with a first real content version.
- Built deep packs for Unit 8, Unit 7, Unit 10 and Unit 6 using the A3 heatmap priorities.
- Added worked examples, graph bank, formula bank, trap bank, Section C templates, mini practice, comparison tables, calculation emergency guidance and study prompts.

### Source basis

- Used `audit/past_paper_heatmap.md`, `audit/a3_coverage_matrix.md`, the War Room v1, archived A2 MegaHub and extracted 2022-2024 A3 source text as control sources.

### Warnings

- Graphs are redraw aids, not exact source-paper replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms.

### Next recommended step

Build `exports/html/eco114_a3_foundations_units_1_to_5.html`, with special focus on Unit 3 because it is very high frequency in the A3 heatmap.


## 2026-06-11 - Markets hub v1 QA polish

### What was checked

- Confirmed branch `feat/eco114-a3-study-hub` and inspected the Markets Hub HTML.
- Checked required top-level sections, sidebar navigation IDs, localStorage-backed progress, dark mode, active recall, answer reveal/collapse and smooth-scroll behaviour in the embedded JavaScript.
- Spot-checked high-risk Unit 8, Unit 7, Unit 10 and Unit 6 calculation and graph logic.

### Issues found

- The Mini Practice Bank had correct counts but several prompts were too generic for exam drilling.
- Unit deep-pack sections needed clearer study routes, most-examinable-pattern boxes and saved mastery checklists.
- Several Section C templates used a generic structure where topic-specific calculation and graph labels would be more useful.

### Fixes made

- Added a near-top `First 2 hours with this Markets Hub` route.
- Added a saved `Markets 80%+ minimum mastery checklist` with concrete Unit 6/7/8/10 capabilities.
- Added study-route, most-examinable-pattern and 80%+ checklist boxes to each Unit 8, Unit 7, Unit 10 and Unit 6 deep pack.
- Replaced the Mini Practice Bank with concrete exam-style T/F, MCQ, calculation, graph and Section C prompts with memo-style answers.
- Upgraded high-priority Section C templates with topic-specific formulas, graph labels, 80%+ paragraphs and mark guidance.

### Remaining limitations

- Graph sketches remain simplified redraw aids rather than exact official diagrams.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

Build `exports/html/eco114_a3_foundations_units_1_to_5.html`, with special focus on Unit 3 and then Units 1, 2, 4 and 5.


## 2026-06-11 - Foundations hub v1 content build

### What was built

- Replaced the scaffold in `exports/html/eco114_a3_foundations_units_1_to_5.html` with a first real content version.
- Built deep packs for Unit 3, Unit 4, Unit 5, Unit 2 and Unit 1 using the A3 heatmap priorities.
- Added worked examples, graph/model bank, formula/logic bank, trap bank, Section C templates, mini practice, comparison tables, reasoning emergency guidance and study prompts.

### Source basis

- Used `audit/past_paper_heatmap.md`, `audit/a3_coverage_matrix.md`, the War Room v1, the Markets Hub v1 for style/function consistency, archived A2 MegaHub and extracted 2022-2024 A3 source text as control sources.

### Content counts

- 40 worked examples.
- 38 formula/logic cards.
- 23 graph/model cards.
- 70 trap cards.
- 29 Section C templates.
- 68 practice questions.

### Warnings

- Graph sketches are redraw aids, not exact source-paper replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms.

### Next recommended step

Run a focused QA polish pass on `exports/html/eco114_a3_foundations_units_1_to_5.html`, then polish `exports/html/eco114_a3_index.html` so it links cleanly to all completed hubs.


## 2026-06-11 - Foundations hub v1 QA polish

### What was checked

- Confirmed branch `feat/eco114-a3-study-hub` and inspected the Foundations Hub HTML.
- Checked required top-level sections, sidebar navigation IDs, localStorage-backed progress, dark mode, active recall, answer reveal/collapse and smooth-scroll pulse behaviour.
- Spot-checked high-risk Unit 3, Unit 4, Unit 5, Unit 2 and Unit 1 worked examples, templates, formulas, graph/model cards, traps and practice prompts.

### Issues found

- The top `First 2 hours` route grouped Unit 3 too broadly instead of separating MRS/MRT from income/substitution effects.
- The top mastery checklist was useful but shorter than the full minimum capability list needed for an 80%+ Foundations pass.

### Fixes made

- Strengthened the `First 2 hours with this Foundations Hub` route to split Unit 3 into feasible set + MRS/MRT and income/substitution effects.
- Expanded the saved `Foundations 80%+ minimum mastery checklist` to 16 concrete capabilities covering GDP, capitalism, opportunity cost, economic rent, production, isocosts, feasibility, MRS/MRT, wage effects, Nash, Pareto and fairness.

### Remaining limitations

- Graph/model sketches remain simplified redraw aids rather than exact official diagrams.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

Polish `exports/html/eco114_a3_index.html` so it functions as the completed A3 control centre linking the War Room, Markets Hub and Foundations Hub cleanly.


## 2026-06-11 - Index control centre polish

### What was built

- Replaced the index scaffold with a completed ECO114 A3 80%+ Control Centre.
- Added main hub cards linking to the Exam War Room, Markets Hub and Foundations Hub.
- Added `What To Open First`, a 14-day study plan, emergency study routes, 80%+ master checklist, topic priority dashboard, graph redraw checklist, formula recall checklist, negative-marking strategy and weekly mistake log.

### Files linked

- `exports/html/eco114_a3_exam_warroom.html`
- `exports/html/eco114_a3_markets_units_6_7_8_10.html`
- `exports/html/eco114_a3_foundations_units_1_to_5.html`

### Checks run

- Confirmed all four HTML files exist.
- Extracted embedded index JavaScript and checked it with `node --check`.
- Checked index hub links and internal anchors.
- Scanned edited files for scaffold/status marker text.
- Ran `git diff --check`.

### Remaining limitations

- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.
- Graph sketches in hubs are redraw aids, not official replicas.

### Next recommended task

Run a final cross-file audit across the Control Centre, Exam War Room, Markets Hub and Foundations Hub.
