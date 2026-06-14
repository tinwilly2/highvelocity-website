# High Velocity Limited — website

A single self-contained file: **`index.html`** (all CSS/JS inline, fonts from Google).
No build step. Open it in a browser to preview; upload it to any host to publish.

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

## Publishing — Cloudflare Pages (chosen route)

GoDaddy only offers a non-editable "Coming Soon" page for free, and £48/year for real
hosting — so we're hosting the static site on **Cloudflare Pages** (free, fast, global
CDN, automatic HTTPS, CLI deploys) and keeping GoDaddy purely as the domain registrar.

### One-time setup
1. Create a free Cloudflare account.
2. From this folder, deploy:
   ```powershell
   npx wrangler login
   npx wrangler pages deploy . --project-name high-velocity
   ```
   This publishes to a `*.pages.dev` URL immediately.

### Custom domain (highvelocity.world)
Two ways to point the GoDaddy domain at Cloudflare Pages:

- **Option 1 — keep GoDaddy DNS (least disruptive):** in Cloudflare Pages → Custom
  domains, add `highvelocity.world`; Cloudflare gives you a CNAME/records to add in
  GoDaddy's DNS panel. Existing email (MX) records stay untouched.
- **Option 2 — move nameservers to Cloudflare (best performance):** add the domain to
  Cloudflare, switch GoDaddy's nameservers to the two Cloudflare ones. **Important:**
  first re-create any existing **MX / email records** in Cloudflare so `info@highvelocity.world`
  keeps working.

### Redeploying after edits
Just re-run `npx wrangler pages deploy . --project-name high-velocity`.
