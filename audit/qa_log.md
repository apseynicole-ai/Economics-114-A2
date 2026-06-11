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
