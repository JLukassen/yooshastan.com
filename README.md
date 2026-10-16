# Yoo Shastan — Independent Software Studio

A standalone, static website for **yooshastan.com**, hosted on GitHub Pages. No framework, backend, JavaScript build, or server needed. Responsive, accessible site with projects for Moka Music Player and KPOPALYPSE NOW.

## Publish via GitHub Pages

1. Create a **new public repository** named `yooshastan.com` under GitHub account `JLukassen`. Keep it **separate** from `kpopalypsenow.com`, which already owns another custom domain.
2. Upload all files in this folder to the **root** of the new repository on `main` (including `index.html`, `styles.css`, `script.js`, `favicon.svg`, `CNAME`, `.nojekyll`).
3. In the new repository, visit **Settings → Pages** → **Build and deployment** → **Deploy from a branch** → choose `main` and `/(root)` → Save.
4. Under **Settings → Pages → Custom domain**, enter `yooshastan.com` and save. The root `CNAME` file already contains that value.
5. At your domain registrar / DNS provider, set the DNS records below; remove *conflicting* parked/old A or AAAA records for `@` (but don't delete MX, TXT, DKIM or other services without checking):

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | JLukassen.github.io |

Optional: GitHub also supports IPv6 `AAAA` records for the apex domain. You can add them later when needed. Don't use a wildcard DNS record. The CNAME **DNS record** for `www` is different from the `CNAME` **file** for the apex domain.

6. Wait for DNS to resolve, return to **Settings → Pages** and enable **Enforce HTTPS** when offered. DNS changes can take up to 24 hours, and certificates may take additional time.
7. Confirm both `https://yooshastan.com/` and `https://www.yooshastan.com/` redirect to the intended site securely.

Validate DNS from Fedora:

```bash
dig yooshastan.com +short A
dig www.yooshastan.com +short CNAME
```

Official GitHub guidance: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Preview locally

```bash
python3 -m http.server 8080
```

Visit `http://localhost:8080/` from the same folder.

## Updating project links

Edit the appropriate anchor links in `index.html`. The page intentionally does not display an active donation or sponsorship link without a verified payment page.

## Relation to other sites

- **yooshastan.com** — studio / future projects hub (this repository)
- **jonlukassen.com** — developer portfolio and career page (separate repository/hosting)
- **kpopalypsenow.com** — K-pop project (separate GitHub Pages repository)
- **Moka Music Player** — Android app and releases at https://github.com/JLukassen/MokaMusicPlayer
