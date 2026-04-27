# GG Inspired Media · Content Studio

A faith-rooted content creation launcher for [GG Inspired Media](https://www.youtube.com/channel/UC8sBtQc9sPlQ5SkyOUvq9QA) — built as a single-page browser homepage that unifies daily content workflows with a touch of the divine.

> *Mercy. Grace. Purpose.* ✦

## Live URL

**[https://corecast8.github.io/gg-inspired-media-launcher/](https://corecast8.github.io/gg-inspired-media-launcher/)**

Bookmark it, set it as your browser homepage, and your studio's a tap away.

## What it does

A self-contained HTML launcher hosted on GitHub Pages, designed to live as a browser homepage. One open brings up:

- A personalized greeting with live clock and a daily-rotating scripture
- One-click workflows: Start Recording (Loom desktop), Daily Devotion, Repurpose Hub, My Channel, Inspiration Break
- A curated app grid — Standard view shows the 5 essentials with descriptive notes; Expanded view adds Office, Canva, ChatGPT, and more
- Smart Prompts that auto-fill ChatGPT with on-brand prompts (newsletter, content calendar, slide deck, etc.)
- Studio Drop and Studio Inbox folder pickers wired to Google Drive sync paths
- Live status pills for camera, mic, internet, and battery
- A "close all tabs I opened" cleanup button
- A hidden Developer Mode (Shift+click the logo) that surfaces extra tools

## For the user

Just open the URL. Optionally:
- Set as Chrome homepage: Settings → On startup → Open a specific page
- Pin the URL to your taskbar
- Click the camera pill once on first use to identify your gear

When the launcher prompts to open Loom or Office desktop apps, click **Allow** and **Always allow** — those apps will then launch silently on every click.

## For the developer

### Make a change

1. Edit `index.html` locally OR through github.com's pencil editor
2. Commit and push
3. User refreshes — change is live

### Stack

- Single-file vanilla HTML/CSS/JS — no build step, no dependencies
- State persisted in `localStorage` per browser per device
- File access via the File System Access API (Chrome/Edge)
- Custom URL-scheme launches: `loom://`, `ms-outlook:`, `ms-word:`, `ms-excel:`, `onenote:`, `spotify:`
- ChatGPT prompt pre-fill via `?q=` URL parameter

### Migrations

The launcher silently upgrades existing user state when the schema changes — adding new app tiles, replacing old prompt text, patching missing fields. Don't remove the migration blocks unless you want to nuke saved state on next load.

### Testing

Visual changes work fine when opening `index.html` directly via `file://`. Full-fidelity testing (custom-protocol launches, etc.) requires a real HTTPS origin — use the GitHub Pages URL.

## Theme

Deep cosmic purple background with gold accents and a subtle twinkling starfield. Cormorant Garamond for the elegant bits, Montserrat for the workhorse type. GG Inspired Media branding embedded throughout.

## Repo

```
.
├── index.html          # the entire launcher — UI, logic, embedded logo
└── README.md
```

## License

Private project.
