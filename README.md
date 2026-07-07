# Victor Barbuta — Portfolio

A single-file, dependency-free personal portfolio website. Just `index.html` — open it, edit it, deploy it anywhere.

## Preview locally
Double-click `index.html`, or run:
```
start index.html
```

## Add your photo
Drop an image named **`photo.jpg`** into this folder (next to `index.html`).
It automatically replaces the hooded-hacker placeholder in the hero — no code changes needed.
- Works with `.jpg` or `.png` (if you use png, rename the `src="photo.jpg"` line in `index.html`).
- Best result: a portrait, roughly square-to-4:5, ~800×1000px.
- Until you add it, the stylized hacker avatar shows automatically.

## How to edit
Everything is in `index.html`:
- **Text/content** — search for the words you want to change and type over them.
- **Colors & fonts** — edit the `:root { ... }` block at the top of `<style>`.
- **Links** — replace `mailto:your@email.com` and the `#` placeholders in the Contact + Projects sections with your real GitHub / LinkedIn / TryHackMe URLs.

## Fill these in as you grow (keep it honest!)
- Real CTF writeups & lab projects (the "Projects & writeups" section)
- Certifications as you earn them (the "Journey" timeline)
- Your actual contact + social links

## Deploy for free (pick one)
### GitHub Pages
1. Create a repo, push this folder.
2. Repo → Settings → Pages → Source: `main` branch, `/root`.
3. Live at `https://<username>.github.io/<repo>`.

### Netlify / Cloudflare Pages
- Drag-and-drop this folder onto app.netlify.com/drop — done in seconds.

### Custom domain
Both support connecting a domain like `victorbarbuta.com` for a professional touch.
```
