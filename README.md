# kehillahlabs.org

Static website for Kehillah Labs, hosted on GitHub Pages. Plain HTML and CSS: no build step.

## Files

- `index.html`: the whole site (single page)
- `styles.css`: styles
- `assets/`: images
- `CNAME`: custom domain for GitHub Pages
- `.nojekyll`: tells GitHub Pages to serve files as-is

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish on GitHub Pages

1. Create a GitHub repository (e.g. `kehillahlabs.org`) and push this folder to its `main` branch.
2. In the repo: **Settings → Pages → Build and deployment**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. At your domain registrar, point `kehillahlabs.org` at GitHub Pages:
   - `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www`: `<your-github-username>.github.io`
4. Back in **Settings → Pages**, confirm the custom domain shows `kehillahlabs.org`, wait for the DNS check, then tick **Enforce HTTPS**.
