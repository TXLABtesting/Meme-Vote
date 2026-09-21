# Meme Vote

A lightweight, bilingual (English / العربية) **team voting game** — think Kahoot-style
party rounds for the office. The host shows a meme and a question on the big
screen, everyone types a colleague's name on their phone, and the results (and
laughter) roll in.

Built as a single, dependency-free HTML page on the
[UAE Government Design System (AEGov DLS)](https://designsystem.gov.ae) colour and
type tokens.

## Run it

No build step. Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

Or enable **GitHub Pages** (Settings → Pages → deploy from `main`) to host it directly.

## What's inside

Three views, switchable from the header:

- **Host screen** — landing → setup (choose the number of rounds, edit each meme
  question) → lobby with a live join counter → round (names stream in as people
  vote) → per-round results → final leaderboard.
- **TV wall** — a grid of every meme with the team's picks, plus a per-meme detail
  view with the full vote breakdown.
- **Phone** — join, waiting room, vote (type a name), vote submitted, all done.

Other touches: an EN/AR language toggle with full RTL support, a live vote
simulation so you can demo the whole flow solo, and no timer — a round closes when
everyone has voted or when the host taps **Show results**.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire app — markup, styles, and vanilla-JS game logic. |
| `logo.png` | Ministry of Cabinet Affairs logo used in the header and phone join screen. |

## Notes

The page loads two things from CDNs: [Phosphor Icons](https://phosphoricons.com)
and Google Fonts (Roboto, Inter, Noto Kufi Arabic, Alexandria). With no network
they degrade gracefully to system fonts and blank icon slots — the layout and game
logic still work.
