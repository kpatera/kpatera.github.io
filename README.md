# Konstantinos Pateras — one-page Hugo site

This is the simplified version: everything is on the home page.

## Daily editing
Edit only:

- `data/site.yml` — almost all text, projects, publications, teaching, supervision, links, MAGNET countries
- `static/images/profile.jpg` — profile photo
- `static/css/main.css` — visual style/colors

## Test locally

```bat
hugo server --disableFastRender
```

## Admin page
The files for `/admin/` are included. The page will load at `/admin/` after deployment, but GitHub login requires a GitHub OAuth/auth proxy or a service such as Netlify Identity/Git Gateway. Without authentication setup, edit `data/site.yml` directly on GitHub.com.

## Deploy
Push the folder contents to `kpatera/kpatera.github.io` and set GitHub Pages to GitHub Actions.

## MAGNET country map

Edit `data/site.yml` and find:

```yml
magnet:
  countries:
    - name: Greece
      code: GR
      status: active
      row: 4
      col: 6
```

To add a new country, copy one country block and change `name`, `code`, `status`, `row`, and `col`.

Allowed statuses are:

- `active`
- `candidate`
- `interested`
- `pending`

The map is a simple editable Europe tile map. Move countries by changing row/column numbers. In the admin page, use **MAGNET → Countries → Add Country**.
