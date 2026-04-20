# qt37t247.github.io

Personal website for **Qian Tang** — ecologist and evolutionary biologist
at the Rowland Institute at Harvard. Built with Jekyll, ready to deploy on
GitHub Pages.

## Structure

```
.
├── _config.yml            # Jekyll site config
├── _layouts/
│   └── default.html       # base HTML layout (header, footer, nav)
├── assets/css/style.css   # clean academic theme
├── index.md               # About / landing page
├── publications.md        # /publications/
├── projects.md            # /projects/
├── cv.md                  # /cv/
├── Gemfile                # Ruby deps (github-pages gem)
└── README.md              # you are here
```

## Run locally

You need Ruby ≥ 3.1. From this directory:

```bash
bundle install
bundle exec jekyll serve --livereload
```

Then open <http://127.0.0.1:4000>.

## Deploy to GitHub Pages

1. Create a new GitHub repo named `qt37t247.github.io` (user site) — or any
   name (project site) if you prefer a `/repo/` path.
2. Push this folder as the repo's default branch:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: personal site"
   git branch -M main
   git remote add origin git@github.com:qt37t247/qt37t247.github.io.git
   git push -u origin main
   ```
3. In the repo's **Settings → Pages**, set *Source* to **Deploy from a branch**,
   branch `main`, folder `/ (root)`.
4. Give GitHub Pages a minute to build. Your site will be live at
   <https://qt37t247.github.io>.

### Project site (alternative URL)

If you deploy to a project repo (e.g. `github.com/qt37t247/my-site`), your
site URL becomes `https://qt37t247.github.io/my-site/`. In that case, edit
`_config.yml` and set:

```yaml
baseurl: "/my-site"
url: "https://qt37t247.github.io"
```

## Customising

- **Avatar.** `index.md` uses an initials placeholder (`QT`). To use a real
  photo, drop `avatar.jpg` into `/assets/img/` and replace the `.avatar` div
  in `index.md` with an `<img>` tag — or give the `.avatar` element a
  `background-image` in `style.css`.
- **Colours.** Edit the CSS variables at the top of `assets/css/style.css`
  (`--accent` is the forest green used for links and highlights).
- **Navigation.** Update the `nav:` list in `_config.yml`.
- **Publications.** The list in `publications.md` was seeded from Google
  Scholar. Add DOIs and PDF links as `<a>` tags inside the `<div class="pub-meta">`
  line of each entry.
- **CV.** Fill in education dates and institutions inside `cv.md`; the
  placeholders are marked with a `.meta` note.
