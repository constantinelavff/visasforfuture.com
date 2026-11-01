# Visas for Future static site

This repository contains the static site for `visasforfuture.com`, prepared for GitHub Pages.

## GitHub Pages settings

- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/(root)**
- Custom domain: **visasforfuture.com**
- Enable **Enforce HTTPS** once GitHub finishes issuing the certificate

## DNS records

Keep all unrelated records, especially mail records and the existing `clients` record. Replace only the apex and `www` website records with:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | `YOUR-GITHUB-USERNAME.github.io` |

Replace `YOUR-GITHUB-USERNAME` before making the `www` record.

Do not cancel Rocket.net until the GitHub Pages URL, custom domain, HTTPS, navigation, contact form, and client-login links have all been verified.
