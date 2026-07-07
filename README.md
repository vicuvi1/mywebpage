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

## Add your résumé
Drop a PDF named **`resume.pdf`** into this folder. The hero's **⬇ Résumé** button opens it in an inline viewer (with a Download button). Until the file exists, the viewer shows blank.

## Social preview image (for LinkedIn / Twitter)
`og-image.svg` is included and referenced in the meta tags. Some platforms (LinkedIn) prefer a **PNG** — if you want a guaranteed preview, open `og-image.svg` in a browser, screenshot it at 1200×630, save as `og-image.png`, and change the two `og-image.svg` references in `index.html`'s `<head>` to `og-image.png`.

## Installable / offline (PWA)
`manifest.json` + `sw.js` make the site installable and work offline — but service workers only run over **https** (e.g. GitHub Pages), not when opened as a local file. It "just works" once deployed.

## Security toolbox
The **Toolbox** section has three live, client-side tools (encoder/decoder, SHA-256 hasher, password strength tester). All run in the browser — no data leaves the page.

## Fun terminal commands (in the About terminal)
`hack`, `crt`, `sound`, and `sudo hire-victor` (🎉 confetti) — plus the achievement toasts they unlock.

## Writeups & blog (edit in one place)
Both the **Projects** cards and the **Blog** section read from a single `library` object near the bottom of `index.html`'s `<script>`.
- To edit a writeup: change the matching entry (`title`, `date`, `excerpt`, `meta`, `body`). `body` is plain HTML.
- To add a project writeup: add a `library` entry, then add `data-open="your-id"` to the project card + its "Read →" link.
- To add a blog post: add a `library` entry, then add its id to the `blogList` array — the card renders automatically.

## Make the contact form send (Formspree — free, no backend)
1. Sign up at [formspree.io](https://formspree.io) and create a new form.
2. Copy your form ID (looks like `xrgjabcd`).
3. In `index.html`, find `action="https://formspree.io/f/your-form-id"` and replace `your-form-id` with yours.
That's it — submissions are emailed to you, and the form shows a success toast without leaving the page.

## Live GitHub widget
The **GitHub activity** section auto-pulls your public repos, stars, and followers from `github.com/vicuvi1`.
To point it at a different username, change `const user = 'vicuvi1';` in the script near the bottom of `index.html`.

## Interactive terminal & easter eggs
- The terminal in the **About** section is live — visitors type `help`, `whoami`, `skills`, `ls`, `cat`, `banner`, `matrix`, etc.
- Hidden: `sudo` → hint → `cat flag.txt` reveals a CTF flag. Another flag is in the browser dev console.
- **Matrix mode:** type `matrix`, or enter the Konami code (↑↑↓↓←→←→ B A). ESC to exit.

## How to edit
Everything is in `index.html`:
- **Text/content** — search for the words you want to change and type over them.
- **Colors & fonts** — edit the `:root { ... }` block at the top of `<style>`.
- **Links** — replace `mailto:your@email.com` and the `#` placeholders in the Contact + Projects sections with your real GitHub / LinkedIn / TryHackMe URLs.
- **Project filters** — each project card has a `data-cat` of `offensive`, `blue`, or `tools`; add cards with the right category and the filter tabs handle the rest.

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
