# Porsche Sell Direct — Project Assets

Place all Porsche Sell Direct case study assets in this folder.

## Folder purpose

Holds static images for the Porsche Sell Direct case study page (`/porsche-sell-direct.html`).

> ⚠️ **Confidentiality:** Only add assets cleared for public sharing. Some project artefacts are omitted due to confidentiality agreements with Porsche Australia.

---

## Recommended file naming

| File name | Used for |
|---|---|
| `hero.png` | Hero section banner / brand visual |
| `listing.png` | Screen 01 — Create a vehicle listing |
| `photo-upload.png` | Screen 02 — Upload vehicle photos |
| `offers.png` | Screen 03 — Track offers & status |

---

## How to swap a placeholder for a real image

In `porsche-sell-direct.html`, each screen currently uses a CSS placeholder inside `.device-frame`. Replace the `.device-placeholder` block with an image:

```html
<div class="device-frame">
  <img class="device-img" src="public/projects/porsche-sell-direct/listing.png" alt="Create a vehicle listing screen" />
</div>
```

For the wide (landscape) frame, keep the `wide` class:

```html
<div class="device-frame wide">
  <img class="device-img" src="public/projects/porsche-sell-direct/offers.png" alt="Track offers and status screen" />
</div>
```

---

## Supported formats

- **Images** — `.png`, `.jpg`, `.webp` (prefer `.webp`)
- Keep originals at 2× for retina; compress to under 300 KB per image.
