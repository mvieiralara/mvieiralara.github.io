# Start here

For normal updates, edit only these files:

- `_data/team.yml` — people
- `_data/research.yml` — research pillars
- `_data/news.yml` — homepage news
- `_data/publications.yml` — publications
- `index.md` — homepage text
- `images/` — photos
- `assets/css/lab.css` — custom styling

The Massively assets are now included. Do not edit `assets/css/main.css` or the files in `assets/js/`.

# BioEfficiency Lab — Jekyll website

This repository is structured for **GitHub Pages with Jekyll** and uses the
**Massively** template by HTML5 UP.

## The files you will normally edit

### Team members

Edit:

```text
_data/team.yml
```

Each person is one YAML block. Change the name, role, category, image filename,
email or description there. The team page is generated automatically.

### Research pillars

Edit:

```text
_data/research.yml
```

The homepage and research page both use this file.

### Main page text

Edit these short Markdown files:

```text
index.md
research/index.md
team/index.md
publications/index.md
teaching/index.md
positions/index.md
contact/index.md
```

Most of the team and research content is generated from `_data`, so you normally
do not need to edit `team/index.md` or `research/index.md`.

### Images

Place images in:

```text
images/
```

Expected filenames:

```text
team-photo.jpg
team-photo2.jpg
photo1.jpg
photo2.jpg
...
photo9.jpg
```

## Files you generally should not edit

```text
_layouts/default.html
_includes/nav.html
_includes/footer.html
assets/css/main.css
assets/css/noscript.css
assets/js/*
```

Your custom style changes belong in:

```text
assets/css/lab.css
```

## Important: copy the Massively assets

The supplied HTML files did not include the original Massively `assets`
directory. Copy these directories from your downloaded Massively template into
this repository:

```text
assets/css/main.css
assets/css/noscript.css
assets/js/
assets/webfonts/
```

Do not overwrite `assets/css/lab.css`.

## Publish with GitHub Pages

1. Create a GitHub repository.
2. Upload all website files to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: `main`
   - Folder: `/ (root)`
5. Save.

GitHub will build the Jekyll site automatically.

For a project repository, set this in `_config.yml`:

```yaml
url: "https://YOUR-USERNAME.github.io"
baseurl: "/YOUR-REPOSITORY"
```

For a repository named `YOUR-USERNAME.github.io`, leave `baseurl` empty.

## Local preview

Install Ruby and Bundler, then run:

```bash
bundle install
bundle exec jekyll serve
```

Open the local address shown in the terminal, usually:

```text
http://127.0.0.1:4000
```

## Template licence

Massively is by HTML5 UP and is released under the Creative Commons Attribution
3.0 licence. Keep the HTML5 UP design credit in the footer.
