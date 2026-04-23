# sejin-kim.github.io

Personal academic homepage for **Sejin Kim** (KIAS, Center for AI and Natural Sciences).

Single-file static site &mdash; no build step required.

## Preview locally

```bash
# Option 1: Python
python3 -m http.server 8000
# then open http://localhost:8000

# Option 2: just open the file
open index.html
```

## Deploy to GitHub Pages

### Option A &mdash; User site at `power817.github.io`

1. Create a new GitHub repository named exactly **`power817.github.io`** (must match your username).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add index.html README.md .nojekyll
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin git@github.com:power817/power817.github.io.git
   git push -u origin main
   ```
3. In **Settings &rarr; Pages**, set:
   - Source: `Deploy from a branch`
   - Branch: `main` / `/ (root)`
4. The site goes live at `https://power817.github.io` in ~1 minute.

### Option B &mdash; Project site (any repo name)

1. Create a repo, e.g. `homepage`.
2. Push the files as above.
3. In **Settings &rarr; Pages**, choose the `main` branch.
4. The site lives at `https://power817.github.io/homepage/`.

### Custom domain (optional)

Add a `CNAME` file to this folder containing your domain (e.g. `sejinkim.com`), then configure the DNS `A` records per [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Update publications

All content is in `index.html`. Find the `<section id="publications">` block and add new entries following the same `<li>` pattern. arXiv IDs link automatically if wrapped in `<a class="arxiv" href="https://arxiv.org/abs/...">`.

## Design notes

- Typography: Crimson Pro (serif body), Inter (UI), JetBrains Mono (numerics).
- Max content width: 760 px. Fully responsive down to 320 px.
- No JavaScript frameworks, no tracking, no external analytics.
- Color palette inspired by Princeton IAS / MIT faculty pages.
