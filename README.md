# POLIS — Pi Lambda Sigma · University of Pennsylvania

Website for Pi Lambda Sigma (POLIS), UPenn's premier nonpartisan pre-professional government society.

## Deploying to GitHub Pages

1. Create a new GitHub repo (e.g. `polis-website` or use your existing one)
2. Push this folder's contents to the `main` branch
3. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Hit Save — GitHub will give you a URL like `https://yourusername.github.io/polis-website`

## Connecting Your Custom Domain (upennpolis.com)

1. In repo Settings → Pages → Custom domain, enter `upennpolis.com`
2. Add a `CNAME` file to the repo root with just: `upennpolis.com`
3. At your DNS provider (Cloudflare), set:
   - A records pointing to GitHub's IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a CNAME record: `www` → `yourusername.github.io`
4. Enable "Enforce HTTPS" in GitHub Pages settings once DNS propagates

## Customizing

- **Logo**: Replace the `Logo Here` placeholder divs with your actual `<img>` tag
- **Employer logos** (`#members`): Replace the `.logo-circle` placeholders with real logos
- **Events**: Update the `.event-item` blocks in the `#events` section
- **Stats**: Update the numbers in `#stats`
- **Quote**: Update the blockquote and attribution in `#quote`
- **Social links**: Update the `href="#"` on the `.social-link` anchors
- **Colors**: All colors are CSS variables at the top of the `<style>` block — tweak `--gold`, `--navy`, etc.
- **Apply link**: Point `#apply` hrefs to your actual application form URL

## File Structure

```
polis-website/
├── index.html      ← entire site (self-contained)
└── README.md
```

Everything is in one file for simplicity. If you want to add subpages (Fellows, Periodical, etc.), just create additional HTML files (`fellows.html`, etc.) and update the nav links.
