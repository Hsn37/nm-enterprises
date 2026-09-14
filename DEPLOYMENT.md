# GitHub Pages deployment

- Repository: https://github.com/Hsn37/nm-enterprises
- Publishing source: `main`, `/` (root)
- Custom domain: `nmenterprises.net`
- Pages settings: https://github.com/Hsn37/nm-enterprises/settings/pages

## Namecheap DNS

In Namecheap, open Domain List → Manage for `nmenterprises.net` → Advanced DNS → Host Records.

Replace the existing website parking / URL redirect record at `@` and the parking CNAME at `www` with:

| Type | Host | Value | TTL |
| --- | --- | --- | --- |
| A | @ | 185.199.108.153 | Automatic |
| A | @ | 185.199.109.153 | Automatic |
| A | @ | 185.199.110.153 | Automatic |
| A | @ | 185.199.111.153 | Automatic |
| CNAME | www | hsn37.github.io | Automatic |

Preserve all email records, including MX, SPF, DKIM, DMARC and any mail-related hostnames. Keep the existing nameservers. At deployment preparation, MX records were `mx1.privateemail.com` and `mx2.privateemail.com`, both priority 10.

These values follow [GitHub's custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

Once DNS resolves to GitHub, wait for Pages to provision its certificate and enable **Enforce HTTPS** in the Pages settings. GitHub notes that DNS propagation and HTTPS availability can take up to 24 hours.

## Updates

```sh
git add index.html styles.css script.js assets
git commit -m "Update website"
git push origin main
```

## Verification

Check the most recent Pages deployment in the repository Actions tab. Confirm the live HTML, styles, script and image assets load, that internal links reach their sections, and that email and phone links target the owner's supplied contact details.
