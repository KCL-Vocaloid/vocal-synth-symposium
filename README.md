# Vocal Synth Symposium 2026 — Website

A single-page static site for the **KCL Digital Humanities Vocaloid Project** launch symposium, ready to deploy on **GitHub Pages**.

## Structure

```
vocal-synth-symposium-2026/
├── index.html          # main page (banner, reservation, schedule, speakers, venue)
├── styles.css          # all styling
├── assets/             # drop your images in here
│   ├── banner.jpg              (horizontal top banner)
│   ├── reserve.jpg             (reservation card visual)
│   ├── room-layout.jpg         (room layout diagram)
│   └── speakers/
│       ├── emma-lin.jpg
│       ├── etiane-cheung.jpg
│       ├── rafal-zaborowski.jpg
│       ├── rongzhi-zhou.jpg
│       ├── uiuc-group.jpg
│       ├── patty-ayukawa.jpg
│       ├── tomohide-ogata.jpg
│       └── zirui-chen.jpg
└── README.md
```

All image spots are wired to `assets/...`. If a file is missing, a labelled placeholder card is shown automatically — so the site never breaks, and you can swap images in one-by-one.

## What to fill in

- **Banner** — `assets/banner.jpg` (horizontal, roughly 16:5 works best).
- **Reservation link** — replace the `href="#"` on the reservation card in `index.html` with the real booking URL, and drop `assets/reserve.jpg`.
- **Welcome video** — when the film is ready, replace the `#welcome-video-embed` block in `index.html` with your `<iframe>` or `<video>` and remove the placeholder frame.
- **Room layout** — `assets/room-layout.jpg`.
- **Speakers** — portrait images in `assets/speakers/`, and replace each `[ Short bio placeholder … ]` line with the real bio.

Speaker names in the schedule are already linked to the corresponding profile card below (e.g. clicking *Emma Lin* jumps to `#s-emma`).

## Deploy on GitHub Pages

1. Create a new repo on GitHub, e.g. `vocal-synth-symposium-2026`.
2. Push the contents of this folder to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin git@github.com:YOUR-ORG/vocal-synth-symposium-2026.git
   git push -u origin main
   ```
3. On GitHub → **Settings → Pages** → *Build and deployment* → **Deploy from a branch** → pick `main` and `/root` → **Save**.
4. Your site will be live at `https://YOUR-ORG.github.io/vocal-synth-symposium-2026/` in a minute or two.

No build step, no dependencies — just static files.

## Editing tips

- Everything is in **`index.html`**; sections are commented so you can find them quickly.
- Colours, spacing, and typography live at the top of **`styles.css`** under `:root` — change the CSS variables to re-theme.
- The programme content can be edited directly in the `.schedule` list; the same speaker anchor IDs (`#s-emma`, `#s-rafal`, etc.) are reused across the schedule and speaker cards.

## Responsible communication

The event page keeps messaging factual and publicly acceptable — programme, speakers, and logistics only. Please keep any social copy in the same tone.
