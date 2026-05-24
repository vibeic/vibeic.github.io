# vibeic.ai

Static landing page for [vibeic/vibe-ic](https://github.com/vibeic/vibe-ic),
served at <https://vibeic.ai>.

## Stack

Zero framework. Plain HTML + CSS + one inline SVG favicon. Built so that
maintenance is trivial and load is instant.

```
.
├── index.html       Main page
├── styles.css       All styling
├── CNAME            vibeic.ai (GitHub Pages custom domain)
├── .nojekyll        Skip Jekyll processing
└── README.md        This file
```

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Hosting

GitHub Pages serves the contents of `main` at the URL declared in
`CNAME` (vibeic.ai). DNS:

```
A      vibeic.ai      185.199.108.153
A      vibeic.ai      185.199.109.153
A      vibeic.ai      185.199.110.153
A      vibeic.ai      185.199.111.153
CNAME  www            vibeic.github.io
```

Enable Pages in repo Settings → Pages → Source: `main`, Custom domain:
`vibeic.ai`, enforce HTTPS.

## Update policy

This site exists only to introduce Vibe-IC and link to the GitHub
repos. Avoid duplicating documentation that lives in
`vibeic/vibe-ic/README.md` — keep this page short, link out for detail.

## License

Site content: CC-BY-4.0. Code snippets within the page reference the
upstream [vibe-ic](https://github.com/vibeic/vibe-ic) repository which
is licensed under Apache-2.0.
