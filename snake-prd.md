# Snake Game — Product Requirements Document

## 1. Product Overview
A browser-based Snake game hosted on a standalone website, monetized through Google AdSense display advertising. Zero-install, zero-login, instant play. The product is an SEO asset: evergreen, low-maintenance, and designed to capture high-intent organic search traffic for queries like "snake game online free."

## 2. Target Users
- **Primary**: Casual gamers aged 13–35 looking for a quick time-killer with no friction
- **Secondary**: Nostalgic users who remember Snake from Nokia phones
- **Acquisition channel**: 95%+ organic search; repeat visitors via muscle memory / bookmarks

## 3. Core Features

### 3.1 Gameplay
- 20×20 grid canvas-based Snake game
- Arrow key + WASD controls; on-screen d-pad for mobile
- Adjustable speed (1–5 levels)
- Score counter + session high score
- Game over → instant restart flow
- Wall collision and self-collision detection

### 3.2 Ad Placement Strategy
| Slot | Size | Position | Notes |
|------|------|----------|-------|
| Leaderboard | 728×90 | Above game | First visible element |
| Medium Rectangle | 300×250 | Right of canvas | Always in viewport |
| Leaderboard | 728×90 | Below game | Visible after game over |

- On mobile (<768px): all ads stack vertically, rectangle collapses to 320×50 banner
- Ads must not overlap or shift the game canvas

### 3.3 UI/UX
- Retro monospace aesthetic (dark bg, green snake)
- Space Mono font
- How-to-play instructions below the game
- Page title and meta tags optimized for SEO

## 4. Technical Requirements
- Single HTML file — no build system, no dependencies, no backend
- Google Fonts via CDN (Space Mono)
- AdSense `<ins>` tags with publisher ID and slot IDs swappable
- `<meta>` tags: title, description, og:title, og:description, canonical URL
- Responsive layout via CSS Grid / media queries
- Lighthouse score target: 90+ Performance, 100 Accessibility

## 5. Success Metrics
| Metric | Target (90 days) |
|--------|-----------------|
| Organic sessions/month | 10,000+ |
| Avg. session duration | 3+ min |
| Pages/session | 1 (single page) |
| Ad CTR | 0.5–1.5% |
| Page RPM | $1–3 |

## 6. Out of Scope (v1)
- User accounts / authentication
- Multiplayer
- Mobile app
- Backend leaderboard
- Payment / subscription tier
