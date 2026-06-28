# Publications

This repository collects Jiayu Li's publication PDFs and academic CV source files.

## Repository structure

```text
.
├── CV/
│   ├── main.tex        # Original CV LaTeX template/source
│   ├── CV_2026.tex     # Updated 2026 CV source
│   ├── CV_2026.pdf     # Compiled 2026 CV
│   └── latexmkrc       # Local latexmk configuration
├── publications/
│   ├── 2015/           # Published papers by official publication year
│   ├── 2019/
│   ├── 2020/
│   ├── 2021/
│   ├── 2022/
│   ├── 2023/
│   ├── 2024/
│   ├── 2025/
│   ├── 2026/
│   └── arxiv/          # Preprints
└── README.md
```

## Publications archive

Publication PDFs are stored under `publications/` and grouped by year. The current archive contains 27 PDF files:

| Folder | Count | Notes |
| --- | ---: | --- |
| `publications/2015/` | 1 | Published papers |
| `publications/2019/` | 1 | Published papers |
| `publications/2020/` | 3 | Published papers |
| `publications/2021/` | 5 | Published papers |
| `publications/2022/` | 3 | Published papers |
| `publications/2023/` | 3 | Published papers |
| `publications/2024/` | 6 | Published papers |
| `publications/2025/` | 3 | Published papers |
| `publications/2026/` | 1 | Published papers |
| `publications/arxiv/` | 1 | Preprints |

Convention:

- Use the official publication year for journal papers.
- Put preprints that are not yet formally published under `publications/arxiv/`.
- Keep publisher-provided filenames when possible; otherwise use a descriptive title-based filename.

## CV

The CV source files are in `CV/`.

- `CV/main.tex` is the original template/source and should be kept unchanged unless intentionally updating the base template.
- `CV/CV_2026.tex` is the working 2026 CV source.
- `CV/CV_2026.pdf` is the compiled PDF generated from `CV_2026.tex`.

To compile the 2026 CV:

```bash
cd CV
latexmk -pdf -interaction=nonstopmode CV_2026.tex
latexmk -c CV_2026.tex
```

The cleanup step removes LaTeX auxiliary files while keeping `CV_2026.tex` and `CV_2026.pdf`.

## Maintenance notes

- When adding a new publication PDF, place it in the corresponding year folder or in `publications/arxiv/` for preprints.
- When updating the CV publication list, keep entries in reverse chronological order, with preprints before formally published papers from the same year.
- Mark co-first authors and corresponding authors consistently in the CV.
- Keep Jiayu Li's name bolded and underlined in publication entries.
- After each CV compilation, clean temporary LaTeX files with `latexmk -c`.
