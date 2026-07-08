# Victor Barbuta — Portfolio

A single-file, dependency-free personal portfolio. Bold, modern, dark. Just `index.html` — open it, edit it, deploy it anywhere.

## Preview locally
Double-click `index.html`, or run `start index.html`.

## The 4 things to make it yours
1. **Photo** — drop `photo.jpg` in this folder (auto-replaces the "VB" placeholder). Portrait, ~800×1000px.
2. **Résumé** — drop `resume.pdf` in this folder (the "Download résumé" button downloads it).
3. **Contact form** — sign up at [formspree.io](https://formspree.io), create a form, and replace `your-form-id` in the `<form action>` with your ID.
4. **Links** — replace `mailto:your@email.com` and the `#` LinkedIn / TryHackMe placeholders in the Contact section.

## Editing content
Everything is in `index.html`:
- **Text** — search for the words and type over them.
- **Colors** — the `:root { ... }` block at the top of `<style>` (one gradient drives the whole accent system).
- **Projects & writeups** — edit the `projects` array in the `<script>`. Each has `id`, `cat` (`offensive` / `blue` / `tools`), `title`, `tags`, `desc`, and a `body` (HTML). The grid, filters, and detail modals all render from it.
- **GitHub widget** — pulls live from `github.com/vicuvi1`. Change `const user = 'vicuvi1'` to your handle.

## Deploy for free
### GitHub Pages
Settings → Pages → Source: **Deploy from a branch** → `main` / `/(root)` → Save.
Live at `https://vicuvi1.github.io/mywebpage/`.

### Netlify / Cloudflare Pages
Drag-and-drop this folder onto app.netlify.com/drop.

## Design notes
Dark, typography-led, glassy cards, one refined indigo→violet→pink gradient. Light/dark toggle included (defaults dark). Respects `prefers-reduced-motion`, keyboard-accessible modals, scroll-spy nav. No heavy background effects — intentionally calm.
