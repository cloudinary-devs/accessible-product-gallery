# Accessible Product Gallery

A demonstration of [Cloudinary Product Gallery's](https://cloudinary.com/documentation/product_gallery) accessibility features.

## How to run

This is a plain static project with no build step required.

**Open directly in a browser:**
Download or clone the repository, then open `index.html` in any browser.


## What to look for in the code

All configuration is in the `<script>` block inside `index.html`. The key accessibility-related properties are:

- **`focus: true`** — moves keyboard focus directly into the gallery when the page loads, so keyboard and screen reader users don't have to tab through the rest of the page first.
- **`zoom: true`** — enables the zoom feature; the popup zoom type (`zoomProps.type: "popup"`) keeps the zoomed view accessible within the page rather than opening a new window.
- **`navigationButtonProps`** — navigation and zoom buttons are given high-contrast colors (`#ffffff` icon on `#000` background) and a generous size (`52px`) to meet WCAG touch target and contrast guidelines.
- **`navigation: "always"`** — navigation arrows are always visible rather than appearing only on hover, which benefits keyboard and switch-access users.
- **`accessibilityProps.mediaAltSource: "contextual"`** — instructs the gallery to generate descriptive alt text for each image from contextual metadata rather than leaving it empty.
- **`videoProps.controls: "play"`** — exposes a visible play/pause control for the video asset so it can be operated without a mouse.

The CSS in `index.css` is minimal and intentionally avoids hiding or overriding focus indicators.
