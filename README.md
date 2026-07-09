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

- `index.html`: homepage
- `style.css`: shared styling
- `project-*.html`: project detail pages
- `interest-*.html`: personal interest detail pages
- `assets/images/`: local image assets
