# Full-Screen Background Image Page

A single-page HTML/CSS project that shows a photo as a full-screen background with a semi-transparent text banner over it. It is a small exercise in using CSS background properties and `rgba` colors.

## Files

| File | Description |
|------|-------------|
| `index.html` | The complete page (HTML and CSS in one file) |
| `Capture.JPG` | Background photo: sea-stack rock formations with a natural arch at sunset, with their reflection on a wet beach |

## What It Shows

- A background photo covering the whole page
- A banner (`.a`) placed about 60% of the way down the screen
- The banner has a semi-transparent white background, so the photo shows through
- Large centered heading: **Mountain View**
- Centered caption: "We can see the beautiful view of nature"

## Key CSS Features

| Feature | Where | Purpose |
|---------|-------|---------|
| `background-image: url(Capture.JPG)` | `body` | Sets the photo as the page background |
| `background-size: cover` | `body` | Scales the image to fill the screen without stretching it |
| `height: 100vh` | `body` | Makes the page as tall as the browser window |
| `margin-top: 60vh` | `.a` | Pushes the banner down toward the lower part of the screen |
| `rgba(252, 252, 252, .5)` | `.a` | White at 50% opacity so the photo shows behind the text |
| `font-size: 10ch` | `h1` | Sizes the heading using the width of the "0" character |
| `*{ margin: 0; padding: 0 }` | global | Removes default browser spacing |

## Project Structure

```
.
├── index.html
├── Capture.JPG
└── README.md
```

Keep `index.html` and `Capture.JPG` in the same folder, because the image is referenced by file name only. The name is case-sensitive on some servers, so keep it as `Capture.JPG`.

## Getting Started

No installation or build step is needed.

1. Put `index.html` and `Capture.JPG` in the same folder.
2. Open `index.html` in any modern web browser.

## Customizing

| To change | Edit |
|-----------|------|
| Background photo | The `url(...)` in the `body` rule |
| Banner position | `margin-top` in `.a` |
| Banner transparency | The last number in `rgba(...)` (0 = invisible, 1 = solid) |
| Heading and caption text | The `<h1>` and `<p>` inside `.a` |
| Text sizes | `font-size` in the `h1` and `P` rules |

## Tech Stack

- HTML5
- CSS3 (background image, `cover` sizing, viewport units, `rgba`)

## Known Issues

- **Title and photo mismatch:** the heading says "Mountain View", but the photo shows coastal rock formations and a beach, not mountains.
- **Possible cropping:** `background-size: cover` crops the image on screens with a different shape from the photo.
- **No background position or repeat settings:** adding `background-position: center` and `background-repeat: no-repeat` would make the result more predictable.
- **Fixed sizes:** the 40px caption and the large heading can wrap or crowd the banner on small phone screens.
- **Selector style:** the paragraph rule is written as `P` (uppercase). It works, but lowercase `p` is the convention.
- **Extra spaces:** the caption text ends with trailing spaces.
- The page title is the default "Document".

## Possible Improvements

- Rename the heading to match the photo (for example, "Sea Arches"), or use a mountain photo
- Add `background-position: center` and `background-repeat: no-repeat`
- Use `clamp()` or media queries so text sizes adapt to small screens
- Add `background-attachment: fixed` for a parallax-style effect
- Add a dark overlay or text shadow for better readability on bright images
- Set a descriptive `<title>`
