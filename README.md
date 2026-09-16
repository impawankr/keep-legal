# keep. — legal pages

Static Privacy Policy and Terms of Use for the keep. app, ready to publish
on GitHub Pages.

- `index.html` — landing page linking to both documents
- `privacy.html` — Privacy Policy (version 2026-09-16)
- `terms.html` — Terms of Use (version 2026-09-16)
- `_src/` — the body text and shared stylesheet the pages were built from
- `.nojekyll` — tells GitHub Pages to serve the files as-is

The pages link to each other with relative paths, so they work at any URL.

## Publishing

1. Create a new **public** repository on GitHub named `keep-legal`.
   It must be public — GitHub Pages will not serve a private repo on a
   free account, and the store listings need a URL anyone can open.

2. From this folder:

   ```sh
   git init
   git add .
   git commit -m "Privacy Policy and Terms of Use"
   git branch -M main
   git remote add origin https://github.com/impawankr/keep-legal.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save.

4. A minute later the pages are live at:

   - `https://impawankr.github.io/keep-legal/privacy.html`
   - `https://impawankr.github.io/keep-legal/terms.html`

## Where these URLs are needed

- **App Store Connect** — Privacy Policy URL (App Information), and the
  same link in the TestFlight beta information for external testers.
- **Google Play Console** — Privacy Policy URL under App content.
- **In the app** — Settings → Legal links to both.

## Updating

Both documents carry a version string (`2026-09-16`) that matches
`POLICY_VERSION` in the app. The consent ledger records that string against
every grant, so **if you change either document materially, bump the version
in both places** — otherwise the ledger claims people agreed to text they
never saw.
