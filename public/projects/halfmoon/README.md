# Halfmoon — Project Assets

Place all Halfmoon case study assets in this folder.

## Folder purpose

Holds static images for the Halfmoon case study page (`/halfmoon.html`).
The page currently uses CSS-built placeholders styled in the Halfmoon palette — swap them for real exports from the design board when ready.

---

## Recommended file naming

| File name | Used for |
|---|---|
| `hero.jpg` | Hero band imagery (yoga in natural light) |
| `mood-1.jpg … mood-4.jpg` | Reference / moodboard grid (Section 02) |
| `landing.png` | Landing page mockup (Section 05) |
| `web-discovery.png` | Web — course discovery |
| `web-player.png` | Web — lesson player |
| `web-profile.png` | Web — member profile |
| `web-account.png` | Web — account / sign-up |
| `app-splash.png` … `app-profile.png` | Mobile app screens (Section 07) |
| `devices.png` | Responsive device showcase (Section 08) |

---

## Brand palette (source of truth)

| Name | Hex | Role |
|---|---|---|
| Deep Pine | `#2E3B40` | Primary · grounding |
| Mist Blue | `#A9BCC4` | Secondary · calm |
| Clay Rose | `#CFA28D` | Accent · warmth |
| Golden Hour | `#BF9A57` | Accent · energy |
| Soft Linen | `#E9E4DA` | Surface · light |

## Typography
- **Display / headlines** — Fraunces (Light & Italic)
- **Body / interface** — DM Sans

---

## How to swap a placeholder for a real image

The hero band, landing, web cards, and app phones use CSS gradient placeholders.
Replace the placeholder `<div>` with an `<img>`, e.g. for the hero band:

```html
<div class="hero-band-img">
  <img src="public/projects/halfmoon/hero.jpg" alt="Halfmoon brand imagery" style="width:100%;height:100%;object-fit:cover;display:block;" />
</div>
```

## Supported formats
- `.jpg`, `.png`, `.webp` (prefer `.webp`); 2× for retina; compress under 300 KB.
