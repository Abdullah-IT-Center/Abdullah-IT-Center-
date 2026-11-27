# Abdullah IT Center — website

Static site for the YouTube channel. No build step.

## Publish on GitHub Pages
1. Create a repo (e.g. `abdullah-it-center`) and upload `index.html`, `privacy.html`, `.nojekyll`.
2. Repo → **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)` → Save.
3. Your site appears at `https://<username>.github.io/<repo>/` in about a minute.

## Protect your YouTube API key (important)
The key is visible in the page source on any static site. That's normal, but lock it down:
1. Google Cloud Console → **APIs & Services → Credentials** → your key.
2. **Application restrictions → Websites** → add `https://<username>.github.io/*`
   (and your custom domain if you add one).
3. **API restrictions → Restrict key → YouTube Data API v3 only**.

Then nobody can reuse the key on another site or for other Google APIs.

## Things to edit in `index.html` (`CONFIG` block)
- `INSTAGRAM_URL`, `WHATSAPP_URL` — fill in to show those icons (hidden when empty).
- `VIDEO_COUNT` / `PAGE_SIZE` — how many videos load and show at once.
- Topic cards, FAQ text, and the founder quote are plain HTML — change them freely.
