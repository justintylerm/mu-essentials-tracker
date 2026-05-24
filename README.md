# /mu/ Essentials Tracker

A self-contained, single-page web app for crossing off albums from the classic 4chan `/mu/` Essentials chart.

**Live:** _will appear here after GitHub Pages is enabled_

## Features

- Click any album cover to mark it listened — fills with the chart's dark background so it disappears
- **Randomize** — slot-machine animation picks a random un-listened album for you, locks until you cross it off
- **Skip tokens** — earn 1 per 10 albums listened, spend to re-roll
- **Peek mode** — fade crossed-off cells to ~10% so you can see what's underneath without un-crossing
- **Export JPG** — download a snapshot of your current progress for sharing
- **Progress bar** — sticky top bar; hover the counter to see percentage
- All progress saved locally in your browser (`localStorage`) — never leaves your device

## Keyboard shortcuts

- `R` — Randomize
- `Space` — toggle the action menu (or dismiss the randomization view)
- `Esc` — dismiss the randomization view

## How it works

Single HTML file with inline CSS + JS, plus `chart-data.js` which embeds the chart image as a base64 data URL. The chart image is overlaid with a CSS grid of transparent click targets — one per album. Each section's coordinates are stored as percentages of the chart's natural 1781×4325 dimensions, so the layout scales with any viewport width.

State lives in `localStorage` under the `mu-tracker:v2:*` namespace. Nothing is sent to a server.

## Local use

Just open `index.html` in any modern browser — no server needed.

```
file:///path/to/mu-essentials-tracker/index.html
```

## Archive

Previous versions are preserved in `archive/` for reference:

- `archive/v2/` — last stable snapshot before the v3 refactor (right-side button layout)
- `archive/v1/` — first usable version
- `archive/prototype/` — initial throwaway prototype

## Credits

The /mu/ Essentials chart is community-maintained on 4chan's /mu/ board. This tool is just a wrapper around it.
