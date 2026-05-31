# www.PhysicsFuture.com

IIT-JEE & NEET online tutoring platform — notes, videos, tests, Ask AI, teacher & student membership.

## Run locally

```bash
cd physics-tutoring
npm start
```

Open **http://localhost:3847**

Demo logins:
- Student: `student@demo.com` / `student123`
- Teacher: `teacher@physicsfuture.com` / `teacher123`

## Publish (GitHub Pages)

1. Create a repo on GitHub (e.g. `physics-future`).
2. Push this folder:

```bash
git init
git add .
git commit -m "Publish www.PhysicsFuture.com"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/physics-future.git
git push -u origin main
```

3. On GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. After the workflow runs, the site is live at `https://YOUR_USERNAME.github.io/physics-future/`

### Custom domain (www.PhysicsFuture.com)

1. Add `CNAME` in repo (already included: `www.physicsfuture.com`).
2. At your domain registrar, add DNS:
   - **CNAME** `www` → `YOUR_USERNAME.github.io`
3. In GitHub Pages settings, set custom domain to `www.physicsfuture.com` and enable HTTPS.

## Live AI (optional)

Copy `server/.env.example` to `server/.env` and add API keys. For production API, host `server/server.js` on Render, Railway, or similar and point `js/ai-client.js` `API_BASE` to that URL.

Without a server, **Ask AI** uses built-in demo mode on the static site.

## Get found on Google

See **[GOOGLE.md](GOOGLE.md)** for Search Console setup. The site includes `robots.txt`, `sitemap.xml`, and SEO meta tags.
