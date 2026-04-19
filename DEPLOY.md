# How to Publish Your Website

## Option A — View locally (no internet hosting)

Just double-click `index.html`. Your default browser opens it. Done.

## Option B — Publish free on GitHub Pages (recommended)

Your site URL will be: `https://<your-username>.github.io`

### One-time setup

1. Create a GitHub account at https://github.com
   - Pick a clean username — it becomes your URL.
2. Install Git for Windows: https://git-scm.com/download/win (accept all defaults).
3. Create a new repository named **exactly** `<your-username>.github.io`
   - Must be **Public**.
   - Don't add README or license at creation.

### Upload your files (easy, no command line)

1. On the empty repository page, click the **"uploading an existing file"** link.
2. Drag `index.html`, `cv.pdf`, and (once you have one) `profile.jpg` into the browser.
3. Commit message: "Initial site". Click **Commit changes**.

### Turn on GitHub Pages

1. Go to **Settings → Pages** (left sidebar of your repo).
2. Source: **Deploy from a branch**.
3. Branch: `main`, folder: `/ (root)`. Click **Save**.
4. Wait 1–2 minutes. Visit `https://<your-username>.github.io`.

### Updating the site later

Edit files locally, then re-upload via the GitHub web UI (overwrites old ones).
Or use Git from the command line:

```
cd "C:\Users\RezaKolasangiani\OneDrive - Mass General Brigham Incorporated\Personal website"
git add .
git commit -m "Update site"
git push
```

## Option C — Alternative free hosts

- **Netlify Drop** (https://app.netlify.com/drop) — drag the whole folder, get a URL in seconds. No account needed for quick tests.
- **Cloudflare Pages** — connects to GitHub, free, custom domain support.
- **Vercel** — same idea, also free.

## Custom domain (optional, costs ~$12/year)

Once live on GitHub Pages, you can point a domain like `rezakolasangiani.com` at it:

1. Buy domain at Namecheap, Google Domains, or Cloudflare.
2. In repo **Settings → Pages → Custom domain**, enter your domain.
3. At your domain registrar, add a CNAME record pointing to `<your-username>.github.io`.
4. Enable "Enforce HTTPS" back in the Pages settings.

## Troubleshooting

- **Fonts/icons look wrong** → check your internet connection (CDNs need to load).
- **"RK" showing instead of photo** → add a file called `profile.jpg` to the folder.
- **GitHub Pages shows 404** → repo name must exactly match `<your-username>.github.io`, and it must be Public.
- **Changes don't appear** → GitHub Pages caches aggressively; hard-refresh with Ctrl+F5.
