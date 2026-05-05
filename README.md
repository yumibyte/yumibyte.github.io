# yumibyte.github.io

Personal site (Jekyll + Minima) for GitHub Pages.

## Edit content

| What | Where |
|------|--------|
| Bio / intro | [`_data/bio.yml`](_data/bio.yml) |
| Work experience | [`_data/experience.yml`](_data/experience.yml) |
| Project cards on `/projects/` | [`_data/projects.yml`](_data/projects.yml) |
| Long-form project write-ups | [`projects/*.md`](projects/) |

After changing `_data/projects.yml`, add a matching file under `projects/<slug>.md` with `permalink: /projects/<slug>/`.

## Publish

1. Create a **public** GitHub repository named **`yumibyte.github.io`** under account **`yumibyte`**.
2. Push this repo to `main`:

   ```bash
   cd /path/to/personal-site
   git init
   git add .
   git commit -m "Initial GitHub Pages site"
   git branch -M main
   git remote add origin https://github.com/yumibyte/yumibyte.github.io.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment** → deploy from branch **`main`** and folder **`/` (root)**.
4. Site URL: **https://yumibyte.github.io/** (may take a minute after the first build).

## Local preview

Requires **Ruby 3.0+** (e.g. via [rbenv](https://github.com/rbenv/rbenv) or [mise](https://mise.jdx.dev/)) and Bundler. A `.ruby-version` file is included for version managers.

```bash
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`.
