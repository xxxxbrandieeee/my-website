# jzhi.app — personal website

Personal academic site for Jiayin Zhi (CS PhD student, University of Chicago).
Plain HTML/CSS — no build step, no dependencies.

```
index.html      About, News, Selected Works
paper.html      Full publication + workshop list
css/style.css   All styling
assets/         Portrait and paper thumbnails
```

## Editing

- **New paper / news item** — edit the HTML directly. Entries are plain
  `<article class="work">` and `<p>` blocks; copy the nearest one and change
  the text. Nothing is generated.
- **Colors and type** — the CSS custom properties at the top of
  `css/style.css` (`--accent`, `--sans`, `--serif`, `--page`).

## Local preview

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deployment

Hosted on GitHub Pages from the `main` branch. Pushing to `main` publishes.

To serve at `jzhi.app` instead of `xxxxbrandieeee.github.io`:

1. Add a file named `CNAME` at the repo root containing `jzhi.app`.
2. Point the domain's DNS at GitHub Pages — four `A` records for the apex
   (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
   `185.199.111.153`) and a `CNAME` for `www` → `xxxxbrandieeee.github.io`.
3. In repo Settings → Pages, set the custom domain and enable "Enforce HTTPS".
