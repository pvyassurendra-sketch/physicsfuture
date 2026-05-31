# Fix: "Your verification file was not found"

Google shows this when you chose **HTML file** verification but the file is missing online.

---

## Fix A — Use HTML tag instead (recommended)

You do **not** need a separate file.

1. Open [Google Search Console](https://search.google.com/search-console) → your property.
2. **Verification** → **Try another method** (or add property again).
3. Choose **HTML tag** (not "HTML file").
4. Copy only the code inside `content="..."`, for example:  
   `aBcDeFg1234567890abcdefghijklmnop`
5. In `index.html` line 13, replace `YOUR_GOOGLE_VERIFICATION_CODE` with that code.
6. **Upload / redeploy** your whole site (Netlify drag-drop, GitHub, or hosting).
7. Open your live homepage → View Page Source → search for `google-site-verification` — code must appear.
8. Click **Verify** in Search Console.

---

## Fix B — HTML file method (if you keep that method)

Google asks for a file with an **exact name**, e.g. `googlee8f4a2b1c3d4e5f6.html`

### Step 1 — Get the exact name from Google

Search Console → Verification → **HTML file** → download or note the filename.

Example: `googlee8f4a2b1c3d4e5f6.html`

### Step 2 — Create the file in your project

In folder `physics-tutoring` (same folder as `index.html`), create a new file:

**Filename:** exactly as Google shows (case-sensitive).

**File content:** one line only (Google gives you this line):

```
google-site-verification: googlee8f4a2b1c3d4e5f6.html
```

(Use YOUR filename in both the file name and this line.)

### Step 3 — Upload again

Upload the **entire** folder to Netlify / GitHub / hosting so the file is at the **website root**:

```
https://YOUR-LIVE-SITE/googlee8f4a2b1c3d4e5f6.html
```

NOT inside a subfolder.

### Step 4 — Test before Verify

Open that URL in Chrome. You must see the one-line text.  
If you get 404, Google will fail.

### Step 5 — Click Verify in Search Console

---

## Common mistakes

| Problem | Solution |
|--------|----------|
| Site only on your Mac | Upload to Netlify/GitHub/hosting first |
| Search Console URL is `physicsfuture.com` but site is on `netlify.app` | Add property for the **same URL** that actually works in browser |
| File in wrong folder | Put file next to `index.html` at root |
| Meta tag still says `YOUR_GOOGLE_VERIFICATION_CODE` | Replace with real code and redeploy |
| Did not redeploy after edit | Drag folder to Netlify again or push to GitHub |

---

## Which URL did you register?

In Search Console, the property must match where the site really lives:

- `https://www.physicsfuture.com` → domain must point to your host
- `https://username.github.io/physics-future/` → file must be under that path

After you have the live URL, update `sitemap.xml` and `meta name="site-base"` to match.
