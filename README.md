# QuietReview Website

Static marketing site for QuietReview — independent, plain-language solar
proposal reviews. Plain HTML/CSS, no build step, no framework. Deploys
directly to Vercel as-is.

## Structure

```
index.html            Homepage
style.css              Shared stylesheet (design system, colors, type)
assets/
  quietreview-logo.png     Full wordmark logo
  quietreview-mark.png     Circular icon mark only (nav, footer, favicon)
  samples/                 Free sample report PDFs (linked from homepage)
```

More pages (order.html, about.html, terms.html) will be added the same way —
drop the file in the root, link to it, done.

## Preview locally

No server required. Just open `index.html` directly in a browser, or for a
closer-to-production preview:

```
npx serve .
```

## Deploy (GitHub → Vercel)

1. **Create a GitHub repo.** On github.com, click "New repository," name it
   `quietreview-website`, leave it empty (no README/license), and create it.
2. **Push this folder to it.** From inside this folder:
   ```
   git remote add origin https://github.com/<your-username>/quietreview-website.git
   git branch -M main
   git push -u origin main
   ```
3. **Connect Vercel.** Go to vercel.com and sign up/log in with your GitHub
   account — this is the fastest path since it links automatically.
4. **Import the project.** From the Vercel dashboard: "Add New… → Project,"
   select `quietreview-website` from the repo list, and click **Deploy**.
   Vercel auto-detects this as a static site — no framework or build command
   needed. Leave those settings blank/default.
5. **You'll get a live URL immediately**, something like
   `quietreview-website.vercel.app`. Every time you push a new commit to
   `main`, Vercel automatically redeploys.
6. **Custom domain (later):** once a domain is purchased, add it under the
   Vercel project's Settings → Domains and follow the DNS instructions shown
   there.
