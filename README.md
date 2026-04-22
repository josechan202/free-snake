# Snake Game — Free Browser-Based Snake

A single-file, deployable Snake game website built to monetize with Google AdSense. No framework, no build step, no backend. Just one HTML file.

## What's in this repo

| File | Description |
|------|-------------|
| `snake.html` | The complete game + ad layout, ready to deploy |
| `snake-prd.md` | Product Requirements Document |
| `snake-feature-research.md` | User feature research + SEO keyword analysis |
| `README.md` | This file |

---

## Quick start

1. Open `snake.html` in any browser — it works immediately with no setup.
2. To go live, deploy it to any static host (see [Deployment](#deployment)).
3. Swap in your AdSense IDs (see [Monetization](#monetization)).

---

## Gameplay

- **Steer**: Arrow keys, WASD, on-screen d-pad, or swipe (mobile)
- **Goal**: Eat the red food to grow longer and score points
- **Game over**: Hit a wall or your own tail
- **Speed**: Adjustable slider (1–5) before or during a game
- **High score**: Saved automatically in your browser via `localStorage`

---

## Monetization

The page has three Google AdSense slots pre-wired. To activate them:

**Step 1 — Replace the publisher ID** (appears in the `<head>` script tag and in every `<ins>` tag):
```
ca-pub-XXXXXXXXXX  →  ca-pub-YOUR_ACTUAL_ID
```

**Step 2 — Replace the slot IDs** (one per `<ins>` tag):
```
data-ad-slot="1111111111"  →  your leaderboard slot ID   (728×90, above game)
data-ad-slot="2222222222"  →  your rectangle slot ID     (300×250, beside game)
data-ad-slot="3333333333"  →  your footer slot ID        (728×90, below game)
```

**Step 3 — Update the canonical URL** in the `<head>`:
```html
<link rel="canonical" href="https://yourdomainhere.com/">
```

Ad slots show gray placeholder boxes until AdSense loads, so the layout is always intact.

---

## SEO

Meta tags are already set up targeting high-volume keywords. Before deploying, update:

```html
<title>Snake Game Online Free — Play Classic Snake Unblocked</title>
<meta name="description" content="Play the classic Snake game free online...">
<meta property="og:title" content="...">
<meta property="og:description" content="...">
```

Top keyword opportunities based on research (see `snake-feature-research.md`):

| Keyword | Monthly searches |
|---------|-----------------|
| snake game online | ~72,000 |
| snake game unblocked | ~110,000 |
| free snake game | ~15,000 |
| classic snake game | ~22,000 |

"Unblocked" is the highest-ROI keyword cluster — low competition, high intent from school/work users.

---

## Deployment

The entire site is one file. Any static host works:

**Netlify** (recommended — free tier, instant deploys)
1. Go to [netlify.com](https://netlify.com) → "Add new site" → "Deploy manually"
2. Drag and drop `snake.html` (rename to `index.html` first)
3. Done — you'll get a live URL in seconds

**GitHub Pages**
1. Create a new repo, add `snake.html` renamed to `index.html`
2. Go to Settings → Pages → deploy from `main` branch
3. Live at `https://yourusername.github.io/reponame`

**Cloudflare Pages** — same drag-and-drop flow as Netlify, also free

**Any web host** — upload `index.html` to your public root directory via FTP/SFTP

---

## Customization

All visual variables are in the `:root` block at the top of the `<style>` section:

```css
:root {
  --bg: #0a0a0a;        /* page background */
  --green: #39ff14;     /* snake color */
  --coral: #ff5733;     /* food color */
  --text: #cccccc;      /* body text */
}
```

Change these to retheme the entire site without touching the game logic.

---

## Roadmap (from feature research)

High-priority features to add in v2, based on user demand:

- [ ] Wall wrap-around mode (no walls — beginner friendly)
- [ ] Swipe gesture support on mobile ✅ already included
- [ ] Sound effects (eat + game over, off by default)
- [ ] Color themes / skins selector
- [ ] Daily streak counter (drives return visits)
- [ ] Share score button (organic acquisition)
- [ ] Obstacle/maze mode for difficulty progression

Full prioritized list in `snake-feature-research.md`.

---

## Tech stack

| Layer | Choice |
|-------|--------|
| Language | Vanilla HTML, CSS, JS — no framework |
| Rendering | HTML5 Canvas |
| Font | Space Mono via Google Fonts CDN |
| Ads | Google AdSense |
| Storage | `localStorage` (high score only) |
| Hosting | Any static host |
| Dependencies | Zero |

---

## License

Game mechanics (falling blocks, grid movement) are not copyrightable — see prior art in *Tetris Holding v. Xio Interactive* (2012). This implementation is original code. The "Snake" name and Nokia-era assets are not used. You own this code.
