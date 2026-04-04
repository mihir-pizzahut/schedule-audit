# 🍕 Schedule Audit Tool — AC Region Calgary

AI-powered schedule auditing tool for Pizza Hut stores. Upload schedule screenshots and get instant visual red flag detection.

## Features

- **Visual Dashboard** — Scoreboard, red flags, traffic-light day grid, letter grades per store
- **AI Schedule Analysis** — Claude AI reads your schedule screenshots and checks against all rules
- **Auto External Context** — Automatically checks Calgary weather, Alberta holidays, sports events, government payment days
- **Deal Tracking** — Upload deal/promo screenshots to factor busy periods into audit
- **Custom Rules** — Add, toggle, or remove audit rules anytime
- **Offline Persistence** — Rules, deal notes, and API key saved in localStorage
- **Mobile Ready** — PWA-capable, works on any device

## Setup

1. Clone this repo
2. Go to **Settings** → Add your [Anthropic API key](https://console.anthropic.com/settings/keys)
3. Open `index.html` or deploy to GitHub Pages

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Schedule Audit Tool"
git remote add origin https://github.com/YOUR_USERNAME/schedule-audit.git
git push -u origin main
```

Then enable GitHub Pages in repo Settings → Pages → Source: main branch.

## How It Works

1. **Upload** schedule screenshots for each store
2. **Add deals** (optional) — screenshots + date notes
3. **Configure rules** — toggle on/off, add custom rules
4. **Run Audit** — AI analyzes everything and returns a visual dashboard

The tool makes two API calls:
1. Web search for Calgary weather, holidays, sports events, payment dates
2. Vision analysis of schedule screenshots against all active rules

## Security

- API key stored in browser localStorage only
- Never transmitted anywhere except directly to Anthropic's API
- No backend, no server, no tracking
