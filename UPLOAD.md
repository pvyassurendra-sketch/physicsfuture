# Upload www.PhysicsFuture.com to the Internet

Choose **one** method below. After upload, your site gets a live URL like `https://something.netlify.app` or `https://yourname.github.io/physics-future`.

---

## Method 1 — Netlify Drop (fastest, no Git)

1. Open **[https://app.netlify.com/drop](https://app.netlify.com/drop)** in Chrome/Safari.
2. Sign up free (email or Google).
3. Drag the **entire** `physics-tutoring` folder onto the page.  
   Or use the ZIP: `Documents/physics-future-upload.zip` (unzip first, then drag the folder).
4. Netlify gives you a link, e.g. `https://random-name-123.netlify.app`
5. Open that link — your site is live.
6. (Optional) **Domain settings** → add custom domain `www.physicsfuture.com`

**Update Google SEO after upload:**  
Edit `index.html` → change  
`<meta name="site-base" content="https://www.physicsfuture.com">`  
to your real Netlify URL, and update `sitemap.xml` URLs the same way. Then drag the folder to Netlify again.

---

## Method 2 — GitHub Pages (free, permanent)

### A. Upload in browser (no Git on Mac needed)

1. Go to **[github.com/new](https://github.com/new)** → create repo `physics-future` → Public → Create.
2. Click **Add file** → **Upload files**.
3. Drag **all files and folders** from `physics-tutoring` (index.html, css, js, robots.txt, sitemap.xml, etc.).
4. Click **Commit changes**.
5. Repo → **Settings** → **Pages** → Source: **GitHub Actions** (workflow file is already in the repo under `.github/workflows/pages.yml`).
6. If Actions don’t run, use Source: **Deploy from branch** → branch `main` → folder `/ (root)` → Save.
7. Live URL: `https://YOUR_GITHUB_USERNAME.github.io/physics-future/`

### B. Using Git in Terminal (if Xcode tools installed)

```bash
cd /Users/surendrapathak/Documents/physics-tutoring
git init
git add .
git commit -m "Upload www.PhysicsFuture.com"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/physics-future.git
git push -u origin main
```

---

## Method 3 — Hosting with cPanel / FTP (GoDaddy, Hostinger, etc.)

1. Log in to your hosting control panel.
2. Open **File Manager** → `public_html` (or `www`).
3. Upload **everything inside** `physics-tutoring`:
   - `index.html` (must be in the root of the website)
   - folders: `css`, `js`, `.github` (optional)
   - `robots.txt`, `sitemap.xml`, `CNAME` (if using custom domain)
4. Visit `https://www.physicsfuture.com` (after DNS points to hosting).

---

## Method 4 — Run on your computer (local only, not public)

```bash
cd /Users/surendrapathak/Documents/physics-tutoring
node server/server.js
```

Open **http://localhost:3847** — only you can see it; this is **not** “uploaded” to the internet.

---

## After upload checklist

- [ ] Homepage opens on the live URL
- [ ] `student-login.html` and `teacher-login.html` work
- [ ] Google Search Console → verify with HTML tag in `index.html`
- [ ] Submit sitemap: `https://YOUR-LIVE-URL/sitemap.xml`

## Need help?

Tell me which method you use (Netlify, GitHub, or hosting company) and your live URL — we can fix `sitemap.xml` and SEO tags for that address.
