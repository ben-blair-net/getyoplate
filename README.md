# 🍽️ Get Yo Plate

A lightweight, mobile-first food ordering web app with separate **Customer** and **Owner** interfaces — no backend required. Built as a GitHub Pages demo you can fork, customize, and deploy in minutes.

**[Live Demo →](https://ben-blair-net.github.io/getyoplate)**

---

## Overview

Get Yo Plate simulates a full order flow between a customer and a restaurant owner, all running in the browser. Toggle between roles in the demo bar to see both sides of the experience in real time.

| Role | What they do |
|------|-------------|
| 📱 Customer | Browse the menu and place an order |
| 👨‍🍳 Owner | Receive and manage incoming orders |

---

## Features

- **Dual-role demo** — switch instantly between Customer and Owner views
- **Mobile-first design** — optimized for small screens with pinch-zoom disabled
- **Dark theme** — sleek, dark UI (`#0C0A06` base)
- **Zero backend** — runs entirely client-side; no server or database needed
- **Reset** — one-tap ↺ button to restore the demo to its initial state

---

## Using the Demo

The demo bar at the top lets you explore both sides of the app without separate accounts:

- **📱 Customer** — places an order from the menu
- **👨‍🍳 Owner** — sees and manages the order queue
- **↺ Reset** — clears all state and starts fresh

Switch between views at any time to watch the order flow update live.

---

## Project Structure

```
getyoplate/
├── index.html        # App entry point
├── assets/
│   ├── index.js      # App logic
│   └── index.css     # Styles
└── README.md
```

---

## Customization

To adapt this for a real restaurant:

- **Menu items** — edit the menu data in `assets/index.js`
- **Branding** — update colors in `assets/index.css` (theme base: `#0C0A06`)
- **App name** — change the `<title>` in `index.html`

---

## Tech Stack

- Vanilla JavaScript (no framework dependencies)
- CSS custom properties for theming
- Hosted on GitHub Pages

---

## License

MIT — free to use, fork, and modify.
