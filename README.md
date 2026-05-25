# PuttTrap

A focused putt-logging web app. Built for Casey, 24.x handicap, where 13+ strokes per round are leaking on the green.

**One file. No build. No backend. No dependencies.** Open `index.html` in any modern browser. Everything is stored in browser localStorage.

## What it does

Logs putts hole-by-hole during a round (or 18 practice-green positions). Shows total putts, three-putts, average per hole, ≤6 ft make rate, miss pattern (dominant direction highlighted in amber), and lag putt control. Tracks practice drill scores over time. Trend chart across rounds. Export/import JSON for backup.

## Quick start

1. **Local:** Double-click `index.html` — opens in browser, works immediately.
2. **iPhone home screen:** open in Safari → share button → "Add to Home Screen" → opens full-screen like a native app.
3. **GitHub Pages:**
   ```
   git init
   git add index.html README.md
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/caseywsj/putttrap.git
   git push -u origin main
   ```
   Then in repo settings → Pages → deploy from `main` branch. Live at `https://caseywsj.github.io/putttrap/` in a couple minutes.

## The 18-position practice-green protocol

Faster than a real round and the data is cleaner (no green-reading or wind variables).

- 6 positions from 10–15 ft
- 6 positions from 20–30 ft
- 6 positions from 30–40+ ft

Mix the order. Pace off, read it, hit it, no do-overs. Log every putt — first putt distance, result, putt out from where it stops. Each "hole" = one starting position. Takes ~30–40 minutes.

## The four numbers that matter

1. **Total putts** — target trending toward 38
2. **Three-putts** — target under 4
3. **≤6 ft make %** — target 70%+
4. **Miss direction** — the diagnostic. If "short" dominates, you're under-reading speed on lag putts. If "long," over-reading. If left/right, line/aim issue.

## Practice drills tracked

- **Gate drill at 4 ft** — log best streak
- **Ladder lag** — 9 putts from 30/40/50 ft, log how many finished within 3 ft
- **Clock drill** — 6 balls at 4 ft, log cycles completed

If drill scores improve but round numbers don't, drills aren't transferring — change the practice plan.

## Data

- Stored entirely in browser localStorage (no server, no analytics, no tracking)
- Export to JSON anytime (Practice tab → Export JSON)
- Import from JSON to restore or move between devices

## What's not here yet

- Course/hole tagging (every "hole 7" looks the same right now)
- Round-over-round delta on the stats screen
- Apple Watch companion for tap-to-log
- TheGrint integration
- Practice → round statistical correlation

## License

Personal use. OpenRoads Consulting.
