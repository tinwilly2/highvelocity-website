# High Velocity Limited — website

A single self-contained file: **`index.html`** (all CSS/JS inline, fonts from Google).
No build step. Open it in a browser to preview; `git push` to publish (see below).

## Preview locally

Just double-click `index.html`, or from this folder:

```powershell
start index.html
```

## Real details — all filled in

Live content as of launch:

- **Director:** Martin Williams
- **Company no.:** 15734101 (England & Wales)
- **Registered office:** Innovations House, 19 Staple Gardens, Winchester, Hampshire SO23 8SR
- **Contact email:** info@highvelocity.world
- **LinkedIn:** none yet — links removed; add back when a profile exists.

Optional future polish (not blocking launch): specific years of experience / named
sectors in the About section, and a VAT line in the footer if/when VAT registered.

## Why this supports an "outside IR35" position

A genuine business website is one of the "in business on your own account" indicators.
This site is written to reinforce that: market-facing service advertising, business
voice ("we"/"High Velocity"), references to a **portfolio of clients** (not one),
mention of own equipment / professional indemnity, accountability for **outcomes not
hours**, and full **statutory details** (registered company name, number, registered
office) in the footer. It's supporting evidence, not a silver bullet — keep it true to
how the business actually operates.

## Publishing — GitHub Pages (live)

The site is **live at https://highvelocity.world** (HTTPS enforced), hosted free on
**GitHub Pages**. GoDaddy is the domain registrar only — its free product is a
non-editable "Coming Soon" page, and Cloudflare's wrangler CLI won't install on this
Windows ARM64 machine, so GitHub Pages was the chosen route.

- **Repo:** `tinwilly2/highvelocity-website` (public), branch `master`, served from the
  repo root. This `website/` folder *is* that repo.
- **Deploy / update:** edit files here, then:
  ```powershell
  git add -A
  git commit -m "your message"
  git push origin master
  ```
  Pages republishes within a minute or two.
- **Custom domain:** the `CNAME` file pins `highvelocity.world`. GoDaddy DNS holds four
  apex A records to GitHub Pages (185.199.108.153, .109.153, .110.153, .111.153) plus a
  `www` CNAME to `tinwilly2.github.io`.
- **HTTPS:** GitHub auto-issued a free Let's Encrypt certificate and "Enforce HTTPS" is on,
  so `http://` is 301-redirected to `https://` for all visitors.
