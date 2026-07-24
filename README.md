# hj-ma.github.io

Personal homepage for Haojun Ma.

## Live Site

- Primary URL: https://haojunma.me
- GitHub Pages URL: https://hj-ma.github.io

## Local Preview

From the repository root:

```bash
python3 -m http.server 8010 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:8010/
```

To check whether the preview server is already running:

```bash
lsof -nP -iTCP:8010
```

## Structure

```text
.
├── index.html                  # Homepage
├── style.css                  # Shared site styles
├── project-*.html             # Stable Selected Work URLs
├── interest-*.html            # Stable legacy interest URLs
├── cv_haojun_ma.pdf           # Current public English CV
├── Haojun_Ma_CV_new.pdf       # Backward-compatible CV alias
├── assets/
│   ├── favicon.svg
│   └── images/
│       ├── profile/
│       ├── projects/
│       └── interests/
├── output/                    # Local generated documents; ignored by Git
├── tmp/                       # Local render/build intermediates; ignored by Git
└── internal/                  # Local planning, evidence, and tooling; ignored by Git
```

Public page filenames remain at the repository root because they are already used by
external links and GitHub Pages. Do not move them without adding a compatibility plan.

### Local-only workspace

- `internal/planning/checklists/`: evidence intake and revision checklists
- `internal/planning/logs/`: dated implementation and release plans
- `internal/evidence/`: private or not-yet-public project reports and source artifacts
- `internal/tooling/`: local skill-development or staging files
- `output/pdf/`: LaTeX sources and generated CV/resume PDFs
