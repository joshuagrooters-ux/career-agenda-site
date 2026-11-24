# Career Agenda — In Development landing page

This is a standalone **static public website** designed for GitHub Pages. It contains only approved Career Agenda branding and non-sensitive public-facing text. It has **no access to** and **no connection with** the private JSM prototype, spreadsheets, GitHub private repository, Apps Script, Calendar, or accounts.

## Contents

- `index.html` — responsive one-page website (desktop banner and mobile-friendly lockup)
- `career-agenda-banner.png` — the exact latest banner supplied by the owner
- `career-agenda-icon.png` — person-only square, cropped from the same banner for mobile screens
- `favicon.png` — favicon cropped from the approved person icon

## Safe setup

1. In GitHub, create a **new public repository** named `career-agenda-site`. Do **not** change the visibility of `jsm-prototype`. Do not upload any private JSM code, spreadsheet data, or credentials.
2. Upload the **uncompressed contents** of this folder into the **root** of the new repo. All five files should appear in the repository root. (Uploading the ZIP by itself will not publish the site.)
3. In the new repo go to **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, then choose `main` and `/(root)` and Save.
4. Verify the default GitHub Pages URL works before changing GoDaddy: `https://joshuagrooters-ux.github.io/career-agenda-site/` (actual URL is shown in Settings → Pages).
5. In the new repo's **Settings → Pages → Custom domain**, enter `careeragenda.app` and save. Verify domain ownership in GitHub if prompted.
6. Only after GitHub's custom domain is configured, go to GoDaddy DNS for `careeragenda.app`. Replace the single parked **A** record at `@` with the GitHub Pages apex **A** records currently given by GitHub's official documentation. Retain the existing NS, SOA, TXT/_dmarc, _domainconnect and unrelated records. Configure `www` correctly per official instructions.
7. Verify `https://careeragenda.app/`, HTTPS enforcement, and `www` handling. Do not forward other domains or edit LinkedIn until the main page works.

Official instructions (verify the live values rather than copying outdated values):
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https

**Status:** This is a *build package*, not evidence that a GitHub Pages repository has been created or that a site has been deployed. Do not change DNS until the GitHub Pages URL is verified and the GitHub custom domain is configured.
