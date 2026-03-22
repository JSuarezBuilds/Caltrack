# CalTrack

A minimal, beautiful calorie and macro tracker that runs entirely in your browser. No accounts, no servers, no subscriptions — just a single HTML file.

![No dependencies](https://img.shields.io/badge/dependencies-zero-blue) ![License MIT](https://img.shields.io/badge/license-MIT-yellow)

## Features

- **Animated progress rings** for calories, protein, carbs, and fat
- **Daily macro tracking** with customizable goals
- **Saved foods** — bookmark meals from the AI Coach and re-log them with one tap
- **AI Coach** — search any food (restaurants, dining halls, homemade) and get real macro data powered by Claude with web search
- **Navigable week strip** — tap any day to review past logs, use arrows to browse previous weeks
- **Persistent storage** via localStorage — data survives tab closes and browser restarts
- **Eastern Time aligned** — day resets at midnight ET
- **Mobile-first dark UI** — optimized for phones, works as a home screen PWA on iOS
- **Zero dependencies** — one HTML file, no build step, no frameworks, no server

## Live

**https://jsuarezbuilds.github.io/caltrack/**

## Add to Home Screen (iOS)

1. Open the link above in Safari
2. Tap the share button → "Add to Home Screen"
3. It launches like a native app with a dark status bar

## How It Works

- All data is stored in `localStorage` keyed by date (`ct_YYYY-MM-DD`)
- Goals stored separately (`ct_goals`), saved foods in (`ct_saved`)
- Past days are read-only; only today allows adding/deleting entries
- No data leaves your device

## Note on AI Coach

The AI Coach tab uses the Anthropic API with web search to look up real nutrition data. This feature works when served through Claude's artifact proxy but requires an API backend for standalone hosting. The core tracker (logging, saved foods, goals, history) works fully offline.

## Tech

- Vanilla HTML/CSS/JS — no React, no build tools
- SVG rings with CSS animations
- `toLocaleString` with `America/New_York` timezone for ET alignment
- Google Fonts (DM Sans)

## License

MIT
