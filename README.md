# Yoo Shastan — Independent Android App Studio

Standalone static site designed for **yooshastan.com**. The **public webpage** intentionally contains no real name, personal portfolio links, personal contact details, or GitHub profile/repository links. Its project page for Moka does not link back to a personal development account.

## Preview locally

From this directory:

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080/ in your browser.

## Publish on GitHub Pages using a separate studio identity

**Important:** To reduce public attribution, do not host this site under a GitHub account with your real name. A custom domain alone does not hide the GitHub Pages repository or account ownership, and DNS / GitHub records can still reveal technical links. True anonymity is not guaranteed.

1. Create a separate studio-branded GitHub account (or choose an alternative host that allows a private source repository and custom domains). Follow the hosting provider's terms for account details.
2. Create a **new, separate site repository** there (for example `yooshastan.com`). Don't alter the existing KPOPALYPSE NOW repository.
3. Upload the root files of this folder to your chosen site repo: `index.html`, `styles.css`, `script.js`, `favicon.svg`, `CNAME`, `.nojekyll`.
4. In repository **Settings → Pages**, select **Deploy from a branch** and choose the primary branch's **root** directory. Enter `yooshastan.com` under **Custom domain**.
5. At your DNS provider, create these GitHub Pages apex records and remove **only conflicting website** records (keep email MX/TXT/etc.):

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | YOUR_STUDIO_ACCOUNT.github.io |

Replace `YOUR_STUDIO_ACCOUNT` with the **new studio GitHub username**, not your personal account. The root `CNAME` **file** already contains `yooshastan.com`.
6. When DNS resolves, turn on **Enforce HTTPS** in Pages settings. Check `https://yooshastan.com/` and the `www` redirect.

GitHub Pages guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Protecting your identity

- Consider domain-registration privacy (RDAP/WHOIS redaction), a domain registrar that offers privacy protection, and a separate brand contact address.
- Links to this studio from a personal portfolio are permitted by your chosen one-way linking strategy, but they can still let visitors correlate the studio with the portfolio owner. Do not claim that the project is technically untraceable or fully anonymous.
- Existing Android project listings, accounts, repositories and app-store records may still reveal authorship through cross-links, RDAP history, metadata, or publicly accessible developer information. **Do not interpret this website as guaranteeing anonymity.**
- Before adding a donation provider or Play Store link, review which legal/business names or contact details it publicly displays.
- Use privacy-conscious analytics or none at all. This static website has no analytics or user tracking.

## Updates

Add future **Android app** projects inside `index.html`. Keep non-Android projects on separate sites. No framework or build step is required; push changes to your hosting repo. Add contact/donation links only when you have independent studio accounts whose public identity you have checked. The Moka project currently shows a public beta status without linking to the real-name GitHub repository.

## Editorial scope

This website exclusively features **Android applications**. Its first listed app is **Moka Music Player**. Other websites or creative projects are intentionally excluded; there are no outgoing links to the studio owner's personal domain or GitHub account.
