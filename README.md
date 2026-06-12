# World Cup 2026 — Predictions Tracker

A single, mobile-friendly view of my picks across four World Cup 2026 prediction pools:
Las Migas, FIFA Predictor (Haas), Pollaya, and Gol Predictor.

**Live site:** https://gonzalovn93.github.io/worldcup-2026-tracker/

## What it does
- **Combined tab** — every group-stage game with my pick in all four pools side-by-side.
  Group it by *Sequence*, *Group*, or *Matchday*. A **Result** column shows the real
  score; any pool that nailed the exact score lights up green.
- **Per-pool tabs** — each pool's full predictions on its own.

## Updating
- **Picks** live in `data.js` (`window.WORLDCUP_DATA`).
- **Real results** live in `data.js` (`window.WORLDCUP_RESULTS`) — fill in `"MEX-RSA": "2-1"`
  as games are played, commit, and the live site updates.

Static site — just `index.html` + `data.js`, no build step.
