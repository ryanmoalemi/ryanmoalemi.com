# RyanMoalemi.com Coming Soon

This repo houses the static "coming soon" page for [ryanmoalemi.com](https://ryanmoalemi.com).

## Local preview

```bash
python -m http.server 4000
```

Open http://localhost:4000 in your browser.

## Deploy to GitHub Pages

1. Create a new public repo on GitHub (for example `ryanmoalemi.com`).
2. Push the contents of this folder to the `main` branch of the repo.
3. In the repo settings, go to **Pages** and set **Source** to `Deploy from a branch`, `Branch = main`, folder `/(root)`.
4. Save. GitHub will publish the site at `https://<your-username>.github.io/ryanmoalemi.com/` (or `https://ryanmoalemi.com` once DNS is configured).

## Point the custom domain

1. In the repo, create a file named `CNAME` in the root with this line:
   ```
   ryanmoalemi.com
   ```
2. Commit and push.
3. Back in the GitHub Pages settings, set the Custom domain to `ryanmoalemi.com` and enforce HTTPS.
4. In Namecheap, add DNS records:
   - Type `A`, Host `@`, Value `185.199.108.153`
   - Type `A`, Host `@`, Value `185.199.109.153`
   - Type `A`, Host `@`, Value `185.199.110.153`
   - Type `A`, Host `@`, Value `185.199.111.153`
   - Type `CNAME`, Host `www`, Value `<your-username>.github.io`

Propagation can take up to an hour. Once done, visiting `ryanmoalemi.com` should show the coming soon page.
