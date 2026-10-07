# Hosting and DNS

Hosting: GitHub Pages, deploying from branch `main` of
github.com/ianfoster/ianfoster.org. Every push to `main` republishes the site
within a minute or two.

## Remaining manual step: DNS at Network Solutions

The domain is registered at Network Solutions, currently on their default
nameservers (ns65/ns66.worldnic.com) serving a parking page. To point it at
the site, log in at networksolutions.com → Domains → ianfoster.org → Manage →
DNS / Advanced DNS records, and set:

- Four A records for the apex (`@` / blank host), TTL default:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
  (replacing any existing A/parking records for `@`)
- One CNAME: host `www` → `ianfoster.github.io.`

Propagation typically takes minutes to a few hours. Once GitHub sees the DNS,
it issues the TLS certificate automatically; then enable "Enforce HTTPS" in
repo Settings → Pages (or ask Claude to set it via API).

## Later (optional)

- Move DNS or the whole registration to Cloudflare for at-cost renewals and
  easy subdomains (e.g. notes.ianfoster.org). Not needed now.
