# Realme P3 — Interactive 3D Mockup

A lightweight, dependency-free interactive 3D mockup of a Realme P3-style smartphone, built with plain HTML, CSS, and JavaScript. Drag a slider to rotate the phone in 3D and view the front (display) and back (camera module) faces.

## Features

- Pure CSS 3D transforms (`perspective`, `transform-style: preserve-3d`, `rotateY`) — no external 3D libraries required
- Interactive rotation slider (0°–360°)
- "Flip to back / front" button for a quick toggle
- Two rendered faces:
  - **Front**: display area with a simple home indicator and branding
  - **Back**: dual-camera module and logo placement
- Fully responsive, self-contained in a single file

## Getting started

### Option 1: Open directly
Just open `index.html` in any modern browser. No build step, no dependencies.

### Option 2: Serve locally
```bash
# Using Python
python3 -m http.server 8000

# Then visit
http://localhost:8000
```

## File structure

```
.
├── index.html      # Markup, styles, and the phone structure
├── style.css       # (optional) extracted styles if you split them out
├── script.js       # (optional) extracted rotation logic if you split them out
└── README.md       # This file
```

> Note: in the current version, HTML, CSS, and JS are combined into a single file for simplicity. Feel free to split them into separate files as shown above if you'd like a more conventional project layout.

## How it works

The phone is a `<div>` with `transform-style: preserve-3d`. It contains two absolutely-positioned faces (front and back), each with `backface-visibility: hidden`, positioned 180° apart using `rotateY(180deg)` on the back face. A range input drives the rotation angle in real time via a `transform: rotateY(...)` update on input, and a button snaps the rotation to 0° or 180° for a quick front/back flip.

## Customization

- **Colors / branding**: update the text, icon, and camera module styling inside the front/back face `<div>` elements.
- **Rotation range**: adjust the slider's `min`, `max`, and `step` attributes.
- **Size**: change the `#stage` and `#phone` width/height values to scale the mockup.

## License

This is a fan-made visual mockup created for illustrative/demo purposes and is not affiliated with, endorsed by, or sponsored by Realme or its parent company. All product names, logos, and brands are property of their respective owners.

Feel free to use and modify this code for personal or educational projects.
