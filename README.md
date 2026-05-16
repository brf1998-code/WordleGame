# Wordle Trainer

A self-contained mobile-first web app for training Wordle skills.

## Modes

**Drill** — The app picks 1 or 2 common letters in specific positions (e.g., `S _ _ _ E`). You race to type every Wordle answer that matches. Wrong letters or non-answers are rejected; valid Wordle words that are never answers get a softer rejection so you learn the difference. Optional 60-second or 2-minute timer.

**Heatmap** — A 26×5 grid showing how often each letter appears at each position across all 2,315 Wordle answer words. Tap a cell to see example words. Below the grid: the top 12 best opening words ranked by positional letter coverage.

**Stats** — Drills completed, total words found, best single drill, and your coverage of the answer list (which of the 2,315 answers you've personally encountered). All stored in your browser via localStorage.

## Run locally

Just open `index.html` in a browser. That's it — no build step.

## Deploy on Railway (share with family)

1. Create a new GitHub repo, drop in: `index.html`, `server.js`, `package.json`, this README. Push.
2. On [railway.app](https://railway.app), click **New Project → Deploy from GitHub repo**, select your repo.
3. Railway auto-detects Node, runs `npm start`, and gives you a public URL like `https://your-app.up.railway.app`.

No environment variables needed. Railway provides `PORT` automatically.

### Alternative: even simpler static hosts

The app is a single HTML file — you can also drop it on:
- **Netlify Drop** (drag-and-drop the folder): https://app.netlify.com/drop
- **Vercel** (`vercel` CLI in the folder, hit enter through prompts)
- **GitHub Pages** (push to a repo, enable Pages on `main` branch)
- **Cloudflare Pages** (connect GitHub repo)

## Add to phone home screen

Open the deployed URL in Safari (iPhone) or Chrome (Android) → Share → **Add to Home Screen**. The app uses `apple-mobile-web-app-capable` so it launches fullscreen like a native app.

## Word list source

The ~2,315 answer words and ~12,972 valid guesses come from the original Wordle game source (pre-NYT acquisition). The NYT has since added/removed a few — but the overwhelming majority of future answers will come from this list.
