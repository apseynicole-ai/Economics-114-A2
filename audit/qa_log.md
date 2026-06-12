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


## 2026-06-11 - Final cross-file A3 system audit

### Files audited

- `exports/html/eco114_a3_index.html`
- `exports/html/eco114_a3_exam_warroom.html`
- `exports/html/eco114_a3_markets_units_6_7_8_10.html`
- `exports/html/eco114_a3_foundations_units_1_to_5.html`

### Checks run

- Repository status, branch, recent commit history and exported HTML listing.
- Cross-file relative link audit between Index, War Room, Markets Hub and Foundations Hub.
- Internal anchor/sidebar navigation audit for all four HTML files.
- Embedded JavaScript extraction and `node --check` for all four files.
- localStorage root-key collision audit.
- Required section audit for all four files.
- Content count verification against previous build reports.
- Marker-text scan for scaffold/status terms.
- Source-honesty wording audit.
- `git diff --check`.

### Issues found

- War Room used shorter section labels for the A3 format and formula bank sections than the final checklist expected.
- War Room source-honesty wording did not explicitly use the same redraw-aids and official-module-materials phrasing as the other hubs.
- Markets and Foundations used equivalent AI-warning wording, but not the exact final cross-file phrase.

### Fixes made

- Normalised War Room section headings to `A3 Format and Negative Marking Strategy` and `Formula and Calculation Bank`.
- Normalised source-honesty wording across the War Room, Markets Hub and Foundations Hub.

### Remaining limitations

- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.
- Graph sketches are redraw aids, not official diagram replicas.
- The working tree contains unrelated local dirty/untracked files outside this final audit.

### Final recommended study route

- Start with the Control Centre and complete the 80%+ Master Checklist.
- Spend the first 48 hours on War Room orientation, Unit 8, Unit 7 and Unit 3.
- Use Markets Hub for calculation-heavy weak spots and Foundations Hub for conceptual traps.
- Finish each day by updating the mistake log and redrawing at least three graphs/models from memory.


## 2026-06-11 - Markets v2 unit-tabs build

### What changed

- Created `exports/html/eco114_a3_markets_units_6_7_8_10_v2_unit_tabs.html` as a new unit-first beta file.
- Preserved the original Markets Hub at `exports/html/eco114_a3_markets_units_6_7_8_10.html`.
- Reorganised Units 8, 7, 10 and 6 so each unit tab contains its own command card, core story, definitions, full theory notes, graphs, formula playbooks, worked examples, past-paper patterns, trap bank, Section C templates, practice bank and one-page sheet.
- Added a short global cross-unit revision section only for comparisons and model selection.

### Practice integrity rule added

- Every practice item in the v2 unit tabs includes metadata for tested concept, taught-above reference, formula/graph used and trap tested.
- Practice is placed after the teaching content inside the same unit tab so questions do not rely on material hidden in a global bank.

### Duplicate/filler trap cleanup

- Replaced duplicated global trap-bank style entries with unit-specific trap sets.
- The audit records 70 rewritten or consolidated duplicate/filler traps.

### Files updated

- `exports/html/eco114_a3_markets_units_6_7_8_10_v2_unit_tabs.html`
- `audit/orphan_practice_question_audit.md`
- `exports/html/eco114_a3_index.html`
- `README.md`
- `audit/qa_log.md`

### Remaining limitations

- The v2 file is a beta and should receive a focused QA polish before it replaces the main Markets Hub link.
- Graph sketches remain redraw aids, not official diagram replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

QA polish Markets v2 unit tabs, especially practice wording, tab usability and closed-book graph redraw clarity.


## 2026-06-11 - Markets v2 QA polish and promotion

### Checks performed

- Audited `exports/html/eco114_a3_markets_units_6_7_8_10_v2_unit_tabs.html` for unit self-contained structure.
- Checked Unit 8, Unit 7, Unit 10 and Unit 6 for command card, core story, definitions, theory notes, graphs, formulas, examples, patterns, traps, Section C templates, practice and one-page sheets.
- Ran practice integrity checks against same-tab teaching content.
- Checked duplicate/filler trap and practice wording.
- Checked localStorage root key against the legacy Markets Hub.
- Ran embedded JavaScript syntax, anchor/link, marker text and whitespace checks.

### Issues found

- Theory notes were too compressed for a student using a unit tab as a standalone lesson.
- Practice questions had correct metadata but too much generic wording.
- Some practice metadata used labels that did not literally match earlier teaching text.
- Search could find hidden-tab content without automatically switching to the matching unit tab.

### Fixes made

- Expanded Unit 8 theory on equilibrium, market vs firm, surplus, taxes, incidence, price controls, shifts and long-run zero economic profit.
- Expanded Unit 7 theory on product differentiation, downward-sloping demand, TR/MR, MR=MC, price from demand, profit rectangle, elasticity, markup, DWL and entry barriers.
- Expanded Unit 10 theory on private vs social outcomes, externalities, Pigouvian policy, public goods, Coase bargaining and information failure.
- Expanded Unit 6 theory on firm authority, incomplete contracts, employment rent, reservation options, best response/isocost, no-shirking wage and involuntary unemployment.
- Rewrote the practice banks into concrete unit-specific questions with memos and normalised metadata.
- Improved search behaviour so a match inside a hidden unit tab activates that tab.
- Promoted Markets v2 from beta to the recommended Markets Hub in the index and README, while preserving the legacy Markets Hub link.

### Results

- Self-contained unit audit: passed for Units 8, 7, 10 and 6.
- Practice integrity audit: passed; no orphan practice concepts remained.
- Duplicate/filler audit: passed; no duplicate trap or practice wording remained.
- Promotion: Markets v2 is now recommended for Units 6, 7, 8 and 10.

### Remaining limitations

- Graph sketches remain redraw aids, not official diagram replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

Run browser/visual QA on the promoted Markets v2 file, especially tab switching, search in hidden tabs, print view and mobile readability.


## 2026-06-11 - Markets v2 browser/visual QA

### Browser/visual QA performed

- Reviewed the promoted `exports/html/eco114_a3_markets_units_6_7_8_10_v2_unit_tabs.html` as a local-file study page.
- Checked the visible layout contract: sidebar navigation, top toolbar, unit tabs, active tab state, cards, definitions, graphs, formulas, practice memos and one-page unit sheets.
- Confirmed the file remains unit-first: Unit 8, Unit 7, Unit 10 and Unit 6 each keep their own theory, graphs, formulas, examples, traps, templates and practice inside the unit tab.

### Tabs tested

- Unit 8, Unit 7, Unit 10 and Unit 6 tab wiring remains intact through generated `data-tab` buttons and generated unit IDs.
- Active tab styling remains visible through the `.tabbtn.active` state.
- Only the selected unit is shown on screen; all unit tabs are shown in print.

### Search result

- Search terms checked: tax, MR, employment rent, Pigouvian, price ceiling, elasticity, Nash and public good.
- Markets terms match the relevant unit content.
- `Nash` has no Markets Hub match, which is correct because Nash is in the Foundations Hub.
- Added a visible search note/status line explaining that search scans all unit tabs and jumps to the first matching unit, and that Nash/Pareto/Angela-Bruno belong in Foundations.

### Mobile result

- Added overflow protection for wide tables and long formulas.
- Improved mobile wrapping for toolbar buttons and unit tab buttons.
- Reduced graph height slightly on narrow screens so SVG redraw aids fit better.

### Print result

- Print CSS already hid sidebar/toolbars and expanded hidden details.
- Added clearer print behaviour so all unit tabs print and each unit starts on a new page where possible.

### Dark mode result

- Existing dark mode contrast remained structurally sound.
- Added search-note dark-mode styling so the new note remains readable.

### Active recall / reveal result

- Expand Answers now opens all memo panels and marks answers as revealed so active recall blur does not remain on expanded memos.
- Collapse Answers now closes panels and removes reveal state.

### Issues found

- Search could previously hide all content on a no-match term, which looked like the page had broken.
- Expand Answers did not fully cooperate with active recall blur.
- Wide tables/formulas had no explicit overflow protection for mobile.
- Print mode showed all tabs but did not clearly begin unit tabs on separate pages.

### Fixes made

- Added a search status/help note near the toolbar.
- Updated search JavaScript to report match/no-match status and activate the first matching unit tab.
- Added table/formula overflow and mobile button wrapping CSS.
- Improved print CSS for all-unit printing.
- Updated Expand/Collapse Answers behaviour for active recall.

### Remaining limitations

- A real screenshot-based browser pass was not available in the local automation environment because Playwright was not installed in the current Node runtime.
- Graph sketches remain redraw aids, not official diagram replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

Open the promoted Markets v2 file in the in-app browser and do a quick human visual skim of Unit 8 and Unit 7, then decide whether to apply the same unit-tab architecture to the Foundations Hub.


## 2026-06-12 - Foundations v2 unit-tabs build

### What was built

- Created `exports/html/eco114_a3_foundations_units_1_to_5_v2_unit_tabs.html` as a new unit-first beta file.
- Preserved the legacy Foundations Hub at `exports/html/eco114_a3_foundations_units_1_to_5.html`.
- Reorganised Units 3, 4, 5, 2 and 1 so each unit tab contains its own command card, core story, definitions, full theory notes, models/graphs, formula/logic playbooks, worked examples, past-paper patterns, trap bank, Section C templates, practice bank and one-page sheet.
- Added a short global cross-unit revision section only for comparisons and model selection.

### Architecture change

- The legacy Foundations Hub uses global graph/formula/trap/template/practice banks.
- Foundations v2 keeps the full study path inside each unit tab so a student can study Unit 3, Unit 4, Unit 5, Unit 2 or Unit 1 without jumping around the page.

### Practice integrity rule added

- Every practice item includes tested concept, taught-above reference, formula/model/graph used and trap tested.
- Practice is placed after the teaching content inside the same unit tab.
- `audit/foundations_orphan_practice_question_audit.md` records the practice counts and orphan-status audit.

### Duplicate/filler cleanup

- Replaced repeated global-bank style trap wording with unit-specific trap lists.
- Duplicate/filler traps rewritten into unit-specific traps: 48.

### Markets link consistency patch

- Updated War Room and legacy Foundations toolbar links so the main Markets link points to `eco114_a3_markets_units_6_7_8_10_v2_unit_tabs.html`.
- Preserved secondary legacy Markets links to `eco114_a3_markets_units_6_7_8_10.html`.
- Added a Foundations v2 beta link to the Index while keeping the original Foundations Hub as the main Foundations link until QA polish passes.

### Remaining limitations

- Foundations v2 is beta and still needs a focused QA polish pass before promotion.
- Graph sketches are redraw aids, not official diagram replicas.
- 2025 Afrikaans A3 remains preserved but not text-extracted.
- Unit 9 remains excluded unless lecturer confirms it is examinable.

### Next recommended task

QA polish Foundations v2 unit tabs, especially Unit 3 depth, Unit 4 matrix mechanics, search behaviour, mobile readability and print view.
