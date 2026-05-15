# iLitUp — Marketing Landing Page

Static, self-contained landing page for iLitup.com.

## Structure
- `index.html` — the entire landing page (single file)
- `assets/` — logo images
- `CNAME` — custom-domain file for GitHub Pages

## Publish via GitHub Pages
1. Create a new public repo on GitHub (e.g. `ilitup-site`)
2. Upload all files in this folder to the repo root (`index.html`, `assets/`, `CNAME`, `README.md`)
3. Settings → Pages → Source: `main` branch, root folder → Save
4. Wait 1–2 min for the green "Your site is live" notice
5. Settings → Pages → Custom domain: `ilitup.com` (the CNAME file already does this; verify it's filled in)
6. In GoDaddy → DNS, set:
   - **A records** for `@` pointing to GitHub Pages IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **CNAME** for `www` → `<your-github-username>.github.io`
7. Back in GitHub Pages: tick **Enforce HTTPS** once DNS propagates (10–30 min)

## Publish directly to GoDaddy hosting (no GitHub)
1. Log into GoDaddy → My Products → hosting plan → cPanel
2. Open **File Manager** → `public_html/`
3. Upload `index.html` and the `assets/` folder
4. Visit ilitup.com — done. (No CNAME file needed in this case.)

## Notes
- Page loads Google Fonts (Inter + Fraunces) from CDN — needs internet on first visit, but caches well.
- All other assets are local. No backend, no API keys, no build step.
# ilitup-landing-marketing
