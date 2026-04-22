# Snake Game — Launch Checklist

## AdSense Setup
- [ ] Sign up at google.com/adsense (if no account)
- [ ] Submit domain for AdSense review (approval takes 1–3 days)
- [ ] Copy publisher ID from AdSense dashboard (`ca-pub-XXXXXXXXXX`)
- [ ] Create ad unit #1 — Leaderboard 728×90 (top)
- [ ] Create ad unit #2 — Medium Rectangle 300×250 (sidebar)
- [ ] Create ad unit #3 — Leaderboard 728×90 (footer)
- [ ] Replace all 3 instances of `ca-pub-XXXXXXXXXX` in `snake.html`
- [ ] Replace `data-ad-slot="1111111111"` with top leaderboard slot ID
- [ ] Replace `data-ad-slot="2222222222"` with sidebar rectangle slot ID
- [ ] Replace `data-ad-slot="3333333333"` with footer leaderboard slot ID

## Pre-Publish Edits
- [ ] Update canonical URL → `<link rel="canonical" href="https://YOURDOMAIN.com/">`
- [ ] Update footer copyright → `© 2025 YourSiteName.com`
- [ ] Confirm page title and meta description match your domain/brand
- [ ] Rename `snake.html` → `index.html`

## Hosting
- [ ] Pick static host (Netlify or Cloudflare Pages recommended — both free)
- [ ] Deploy `index.html` (drag and drop on Netlify, or push to GitHub repo)
- [ ] Confirm live URL loads correctly
- [ ] Test on mobile — verify ad layout and d-pad controls work

## Post-Launch
- [ ] Add site to Google Search Console
- [ ] Request indexing for the URL in Search Console
- [ ] Set up Google Analytics (optional but recommended)
- [ ] Verify AdSense ads are serving (can take 24–48 hrs after launch)
- [ ] Check AdSense policy compliance — ensure no ad placement violations
