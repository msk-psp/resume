# Resume — 김민수 (Minsoo Kim)

LaTeX sources for my resume / CV. Korean and English versions are built from shared experience and project fragments.

## Layout

```
.
├── resume_korean.tex       # Korean version entry point
├── resume_english.tex      # English version entry point
├── custom-commands.tex     # Shared LaTeX macros (\resumeSubheading, etc.)
├── fonts/                  # Bundled NanumGothic fonts (so xelatex works without system install)
├── images/                 # Project screenshots referenced from .tex
└── src/
    ├── korean/             # KR-specific sections: heading, core_skills, skills,
    │                       #   career_summary, experience, education, others, coverletter
    ├── english/            # EN-specific sections (mirror of korean/)
    ├── projects_korean.tex         # Brief project section dispatcher (KR)
    ├── projects_english.tex        # Brief project section dispatcher (EN)
    ├── projects_detail_korean.tex  # Detailed project section dispatcher (KR)
    ├── projects_detail_english.tex # Detailed project section dispatcher (EN)
    ├── projects/{korean,english}/         # Per-project brief fragments
    └── projects_detail/{korean,english}/  # Per-project detailed fragments
```

## Build

Requires a LaTeX distribution with `xelatex` (TeX Live, MacTeX, or MikTeX). Korean rendering needs the `kotex` package; bundled NanumGothic fonts are loaded from `fonts/`, so no system font install is needed.

```bash
# One-shot build
xelatex resume_korean.tex
xelatex resume_english.tex

# Or with latexmk (auto-handles multi-pass references)
latexmk -xelatex resume_korean.tex
latexmk -xelatex resume_english.tex

# Clean build artifacts
latexmk -C
```

Built PDFs are gitignored — regenerate locally before sharing.

## Adding a new experience

1. Append a new `\resumeSubheading {...}{...} ... \resumeItemListEnd` block at the **top** of `src/korean/experience.tex` and `src/english/experience.tex`.
2. (Optional) Create a detail fragment under `src/projects_detail/{korean,english}/N_<slug>.tex` and reference it from `src/projects_detail_{korean,english}.tex`.

## Editor

VS Code with the LaTeX Workshop extension works well — it auto-runs `latexmk` on save. Overleaf still works too: upload the repo as a zip.
