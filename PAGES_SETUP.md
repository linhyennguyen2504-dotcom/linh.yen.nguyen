GitHub Pages setup & DNS instructions

1) Enable GitHub Pages
- Go to this repository's Settings > Pages.
- Source: `main` branch, `root` (/) folder. Save.
- Add `CNAME` file at repository root with your custom domain (already added: `linhyennguyen.com`).
- Optionally enable "Enforce HTTPS" after GitHub provisions the certificate.

2) DNS records to point `linhyennguyen.com` to GitHub Pages
- For apex domain (`linhyennguyen.com`), add these A records at your registrar/DNS provider:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153

- Add a CNAME record for `www` to point to `linhyennguyen2504-dotcom.github.io` (your GitHub Pages site):
  - `www` CNAME -> `linhyennguyen2504-dotcom.github.io`

3) Wait for propagation and HTTPS
- DNS changes can take up to 24-48 hours, usually faster.
- GitHub will provision HTTPS automatically after the domain resolves; wait a few minutes to a few hours.

4) Verification
- Visit https://linhyennguyen.com once DNS propagates.
- If you see a 404 from GitHub Pages, double-check Pages source and that `index.html` exists at repo root.

Notes
- If you prefer `www.linhyennguyen.com` as primary, set CNAME for `www` and create an ALIAS/ANAME to point the apex, or set forwarding from apex to www at your registrar.
- I added a placeholder `cv/Linh_Yen_Nguyen_CV.pdf` file; replace it with your real CV PDF of the exact same filename to keep the download link working.
