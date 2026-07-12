# Cosmica Shop

A single-file affiliate landing page for the [Cosmica YouTube channel](https://youtube.com/@CosmicaExplains). No frameworks, no build step — `index.html` is the whole site.

## Edit products (the easy way)

1. Open `manager.html` in your browser (double-click it). It runs 100% locally — nothing is uploaded anywhere.
2. Drag your current `index.html` onto the drop zone (or click to browse).
3. Add, edit, delete, or drag-reorder products. Rows marked **⚠ no affiliate link yet** still need an Amazon link.
4. Paste affiliate links from Amazon SiteStripe — the manager confirms the ASIN when it detects one.
5. Click **⬇ Download updated index.html** and replace your old `index.html` with the downloaded one.

You can also edit the `const PRODUCTS = [...]` array at the top of the `<script>` in `index.html` by hand — that array is the only thing that controls the grid.

## Deploy

### Netlify Drop (fastest)
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag `index.html` (just that file, or a folder containing only it) onto the page.
3. To update: open your site in Netlify → **Deploys** → drag the new `index.html` in.

### GitHub Pages
1. Push this repo to GitHub (`manager.html` is git-ignored, so it stays local — keep it that way).
2. Repo **Settings → Pages → Source: Deploy from a branch** → pick `main` / root.
3. Your site appears at `https://<user>.github.io/<repo>/`. To update, commit and push the new `index.html`.

## Amazon Associates disclosure

Amazon **requires** a visible disclosure on any page with affiliate links. The footer already contains the required wording — *"As an Amazon Associate, Cosmica earns from qualifying purchases."* — **do not remove it**, or your Associates account can be closed.

## ⚠ Never deploy manager.html

`manager.html` is a local admin tool only. It's listed in `.gitignore` so it won't be committed or published — don't upload it to Netlify or any host.
