# iFruit OS — Leonida

**iFruit OS** is a GTA VI-inspired browser-based desktop simulation. It runs entirely in the browser — no server, no install.

> A website, not a real operating system.

---

## Single-file builds

| File | Size | Description |
|------|------|-------------|
| [`learn-1.html`](learn-1.html) | ~739 KB | Complete standalone HTML build |
| [`learn-1.svg`](learn-1.svg) | ~738 KB | Complete standalone SVG build (foreignObject) |

Both files contain the **entire application** — React runtime, all apps, all CSS, all icon artwork — bundled as a single self-contained file. No build step, no server, no CDN required for the shell. (External game embeds and movie posters still need internet.)

### Password

The lock screen password is **`jamesisawesome`**.

---

## CDN distribution links

Once published to GitHub (replace `OWNER/REPO` with your username/repository):

### learn-1.html

```
https://cdn.jsdelivr.net/gh/OWNER/REPO@main/learn-1.html
https://raw.githubusercontent.com/OWNER/REPO/main/learn-1.html
https://rawcdn.githack.com/OWNER/REPO/main/learn-1.html
https://raw.githack.com/OWNER/REPO/main/learn-1.html
https://statically.io/gh/OWNER/REPO/main/learn-1.html
```

### learn-1.svg

```
https://cdn.jsdelivr.net/gh/OWNER/REPO@main/learn-1.svg
https://raw.githubusercontent.com/OWNER/REPO/main/learn-1.svg
https://rawcdn.githack.com/OWNER/REPO/main/learn-1.svg
https://raw.githack.com/OWNER/REPO/main/learn-1.svg
https://statically.io/gh/OWNER/REPO/main/learn-1.svg
```

### GitHub Pages

After enabling Pages (Settings → Pages → main branch / root):

```
https://OWNER.github.io/REPO/learn-1.html
https://OWNER.github.io/REPO/learn-1.svg
```

---

## Apps

| App | Description |
|-----|-------------|
| Eyefinder | Web browser (iframe-based) |
| iHTML | Live HTML/CSS editor with sandbox preview |
| iGames | 155 verified HTML5 games |
| iMovies | Movie/TV browser with poster art |
| iFruit Finder | File/app browser |
| Photos | Leonida photo gallery |
| iFruit Radio | Synthwave music player (Web Audio API) |
| Calendar | Vice City agenda |
| Notes | Persistent notepad |
| iFruit Store | App store UI |
| Weather | Static weather card |
| Calculator | Neon calculator |
| iShell | Simulated terminal |
| Activity Monitor | Live process/CPU/memory display |
| System Settings | Wallpaper, accent, sound, dock |
| About | System info |

---

## Technical notes

### SVG build

`learn-1.svg` uses `<foreignObject>` to embed a full XHTML document inside SVG. This is the only viable approach for a React application in SVG format — pure SVG-native elements cannot replicate a 200 KB bundled application. The file must be opened as a **standalone top-level document** (not embedded via `<img src="...">` or `<object>`) for scripts to execute.

### Module loading

The Vite build emits ES modules with chunk imports. The single-file builds use a blob-URL rewriting strategy: each chunk is converted to a `Blob` → `URL.createObjectURL()` URL, and import specifiers inside other chunks are rewritten to point at those blob URLs. No importmap, no service worker required.

### External dependencies

- **Fonts**: Inter + Space Grotesk from Google Fonts (requires internet on first load; cached thereafter)
- **Game embeds**: hosted at `raw.githack.com`, `scratch.mit.edu`, `cdn.jsdelivr.net`
- **Movie posters**: `image.tmdb.org`
- **Movie streaming**: third-party embed servers (variable availability)

---

## Development

```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # dist/
```

After building, regenerate the single-file distributions:

```bash
node scripts/inline.mjs
```

---

## License

Source code: MIT. Game assets, movie posters and media embeds are third-party content and subject to their respective licenses.
