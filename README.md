# vibeic.github.io

Redirect-only site. Visitors hitting `https://vibeic.github.io/` are
sent to `https://vibeic.ai/`.

The real Vibe-IC landing page lives at <https://vibeic.ai> and is
served from a separate repo (`vibeic/vibeic.ai`).

## Why this exists

`vibeic.github.io` is the GitHub-side fallback URL for the `vibeic`
org. We keep it as a 5-line meta-refresh redirect so:

- Anyone who guesses the GitHub URL still reaches the project.
- The org's Pages slot is occupied (prevents accidental misuse).
- Zero overlap with the real site at `vibeic.ai`.

## How the redirect works

`index.html` does three things in order:

1. `<script>window.location.replace(...)</script>` — instant redirect,
   no history pollution. Works in every modern browser.
2. `<meta http-equiv="refresh">` — fallback for JavaScript-disabled clients.
3. Visible `<a>` link — fallback for both above failing.

`<meta name="robots" content="noindex">` keeps search engines from
indexing this URL — only `vibeic.ai` should appear in SERPs.
`<link rel="canonical">` reinforces the same.

## Update policy

Don't add features here. If you want to change the landing page, do it
in `vibeic/vibeic.ai`. This repo should stay at one HTML file.
