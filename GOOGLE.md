# Publish on Google Search (www.PhysicsFuture.com)

Your site includes **robots.txt**, **sitemap.xml**, and SEO tags so Google can index it.

## Step 1 — Site must be live online

Deploy to GitHub Pages, Netlify, or your host. Google cannot index files only on your computer.

Live URL examples:
- `https://www.physicsfuture.com`
- `https://YOUR_USERNAME.github.io/physics-future/`

If you use GitHub Pages with a project folder, update `meta name="site-base"` and URLs in `sitemap.xml` to match your real URL.

## Step 2 — Google Search Console

1. Open [Google Search Console](https://search.google.com/search-console)
2. Click **Add property**
3. Choose **URL prefix** and enter: `https://www.physicsfuture.com`
4. Verify ownership (pick one method):
   - **HTML tag** — copy the code Google gives you into `index.html` where it says `google-site-verification` (see below)
   - **DNS** — add a TXT record at your domain registrar
5. After verified, go to **Sitemaps**
6. Submit: `https://www.physicsfuture.com/sitemap.xml`
7. Use **URL inspection** → enter your homepage → **Request indexing**

## Step 3 — Google verification tag (in index.html)

Replace `YOUR_GOOGLE_VERIFICATION_CODE` in `index.html` with the content value from Search Console, for example:

```html
<meta name="google-site-verification" content="abc123xyz..." />
```

## Step 4 — Optional (recommended)

- Create a [Google Business Profile](https://business.google.com) for your coaching / tutoring
- Add your phone **9934379825** and website **www.PhysicsFuture.com**
- Link from WhatsApp and social profiles to the live site

## Files included for Google

| File | Purpose |
|------|---------|
| `robots.txt` | Tells Google it may crawl the site |
| `sitemap.xml` | Lists all main pages for indexing |
| `js/google-seo.js` | Canonical URLs on every page |
| Meta tags on `index.html` | Title, description, Open Graph |

Indexing usually takes a few days to a few weeks after you submit the sitemap.
