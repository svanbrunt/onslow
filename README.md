# Onslow Forever ⚾🎩

The deeply unserious history of the Onslow guys' annual baseball-trip pilgrimage.
Live at **https://svanbrunt.github.io/onslow/**

## How this repo works

- **`baseball-trip.html`** — the full source you edit. Scrapbook (shared notes + photos
  via Supabase) is **ON** here (`ENABLE_SCRAPBOOK = true`).
- **`index.html`** — the public static site GitHub Pages serves. Auto-generated from
  the source with the scrapbook **OFF** and the Supabase script removed. **Don't edit
  by hand** — it gets overwritten.
- **`.github/workflows/build-static.yml`** — on every push that changes
  `baseball-trip.html`, regenerates `index.html` and commits it back. Pages redeploys
  automatically.

## To make a change

Edit `baseball-trip.html`, then:

```bash
git add baseball-trip.html
git commit -m "your change"
git push
```

The Action rebuilds `index.html` within a minute and the live site updates.

## To go live with the scrapbook later

Fill in your Supabase URL + anon key near the top of `baseball-trip.html`, set
`ENABLE_SCRAPBOOK = true` (already the default), and decide whether to publish the
scrapbook build instead of the static one. (The current Action always ships the
static, scrapbook-off build to the public site.)
