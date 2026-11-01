# Migration status

Prepared: 2026-11-01 (Europe/Berlin)

## Ready

- Static copies of the homepage, About page, and Contact page
- All WordPress-hosted image assets copied into `assets/`
- `CNAME` set to `visasforfuture.com`
- `.nojekyll`, `robots.txt`, and `sitemap.xml` prepared for GitHub Pages
- Local responsive preview checked for the homepage, About page, and Contact page
- Git repository initialized on branch `main` with an initial commit

## Waiting for account access

1. Sign in to GitHub so the public repository can be created and published.
2. Sign in to the Cloudflare account containing `visasforfuture.com` so only the website records can be changed.

Namecheap currently acts as the registrar. The authoritative DNS is Cloudflare:

- `rose.ns.cloudflare.com`
- `sid.ns.cloudflare.com`

## DNS records that must be preserved

The following public records were observed before cutover:

- MX: `1 smtp.google.com.`
- SPF: `v=spf1 a mx include:mailgun.org a include:_spf.google.com ~all`
- Google verification TXT records: two existing records
- `clients.visasforfuture.com` CNAME: `domains.spp.io.`

The full Cloudflare zone must still be reviewed in the dashboard before changing anything. Only the apex (`@`) website records and `www` should be replaced. Mail, verification, `clients`, and all unrelated records must remain untouched.

## Existing site issues not caused by the migration

- `/privacy-policy/` returns HTTP 500.
- `/terms-of-service/` returns HTTP 500.
- The embedded Wayfront contact form redirects to an expired page and cannot render.
- The client login endpoint still resolves successfully.

Do not cancel Rocket.net until the GitHub Pages URL, custom domain, HTTPS, navigation, and client-login link have been verified after DNS propagation.
