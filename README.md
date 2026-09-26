# Click a Cookie — portfolio

Personal portfolio page for Giulian and the Roblox game **Click a Cookie**.

Single static site: `index.html` + `style.css`. No build step, no framework,
no JavaScript dependencies. The only script is ~40 lines inline for the scroll
progress bar, the header clock, and copy-to-clipboard.

## Play the game

<https://www.roblox.com/games/81217623291156/Click-a-Cookie#!/game-instances>

## Contact

giuli190211@gmail.com

## Local preview

Open `index.html` directly, or serve it:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploy on GitHub Pages

1. Push this folder as-is to a repository named `giulian.github.io`.
2. **Settings → Pages → Build and deployment → Source**: choose *Deploy from a branch*.
3. **Branch**: `main`, **Folder**: `/ (root)`.
4. Save, then push. The site goes live at <https://giulian.github.io>.

If the repository has a different name, point the Pages branch at this folder
and the site will live at `https://<username>.github.io/<repo-name>/`.
Because everything is a relative local asset, no base-path fixups are needed.

## Editing content

- **Game description and feature list** — `<section id="games">` in `index.html`.
- **Roadmap** — `<div class="roadmap">`, items are plain `<li>`s.
- **Email** — the `mailto:` link and the `#mail` element in `<section id="contact">`.
  Update both if the address changes (the copy button reads the visible text).
- **Colours and type scale** — the `:root` custom properties at the top of `style.css`.

## Design notes

Editorial "printed paper" treatment: warm off-white stock, a single terracotta
accent, Fraunces (serif display) paired with Archivo (sans body), and a faint
CSS-only halftone grain. No gradients, glassmorphism, blur-on-scroll reveals,
or emoji-laden iconography — the restraint is the point. All motion is gated
behind `prefers-reduced-motion`.
