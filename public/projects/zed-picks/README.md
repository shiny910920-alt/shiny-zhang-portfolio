# ZED Picks — Project Assets

Place all ZED Picks case study assets in this folder.

## Folder purpose

This directory holds all static images and media for the ZED Picks case study page (`/zed-picks.html`).

---

## Recommended file naming

| File name | Used for |
|---|---|
| `hero.png` | Hero section background / banner image |
| `hero-phones.png` | Three-phone mockup in the hero visual |
| `screen-home.png` | Race Hub screen (Design Solution section) |
| `screen-horse.png` | Horse Detail screen |
| `screen-live.png` | Live Race screen |
| `screen-result.png` | Win / Result screen |
| `screen-leaderboard.png` | Leaderboard screen |
| `wireframe-lofi.png` | Lo-fi wireframe (Interaction Design section) |
| `wireframe-midfi.png` | Mid-fi wireframe |
| `wireframe-hifi.png` | Hi-fi final UI |
| `persona-jordan.jpg` | Persona — Jordan T. (Casual Bettor) |
| `persona-maya.jpg` | Persona — Maya L. (Curious Gamer) |
| `persona-ryan.jpg` | Persona — Ryan K. (ZED Power User) |
| `persona-sophie.jpg` | Persona — Sophie P. (Racing Enthusiast) |
| `design-system.png` | Design system / token overview |
| `journey-map.png` | User journey map diagram |

---

## How to reference assets in zed-picks.html

Use a root-relative path from the portfolio root:

```html
<img src="public/projects/zed-picks/hero.png" alt="ZED Picks hero" />
```

Or as a CSS background:

```css
background-image: url('public/projects/zed-picks/hero.png');
```

---

## Supported formats

- **Images** — `.png`, `.jpg`, `.webp` (prefer `.webp` for performance)
- **Video** — `.mp4` (for prototype demos or race animations)
- **SVG** — `.svg` (for icons or diagrams)

---

## Notes

- Keep originals at 2× resolution for retina displays.
- Compress images before committing — target under 300 KB per image.
- All assets in this folder are served statically alongside the HTML files.
