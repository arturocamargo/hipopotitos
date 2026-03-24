# 🦛 Challenge Tracker PWA — Setup Guide

A beautiful, mobile-first PWA for tracking fitness (or any) challenges between friends or family. Scoreboard, personal dashboards, streaks, heatmaps, confetti.

**Live demo:** https://arturocamargo.github.io/hipopotitos/

---

## What you'll need
- A GitHub account (free)
- A Google account (for the Form + Sheet)
- 20 minutes

---

## Step 1 — Fork the repo

Click **Fork** at the top right of this repo.
Enable GitHub Pages: Settings → Pages → Source: **Deploy from branch → main → / (root)**

Your app will be live at: `https://YOUR-USERNAME.github.io/hipopotitos/`

---

## Step 2 — Create your Google Form

1. Go to [Google Forms](https://forms.google.com) → create a blank form
2. Add these questions:
   - **Short answer:** "¿Quién eres?" (or "Who are you?") — list your players as options (dropdown)
   - **Date:** "Fecha" (Date)
   - **Short answer or Number:** "Minutos de actividad"
   - **Checkboxes:** "Bonus del día" — add your bonus options
3. Link to a Google Sheet: Responses tab → green Sheet icon → create new sheet
4. In the sheet: File → Share → Publish to web → select your responses sheet → CSV → Publish → copy the URL

---

## Step 3 — Edit CONFIG

Open `index.html` and edit the `CONFIG` block at the top of the script:

```javascript
const CONFIG = {
  appName: "My Challenge",      // ← your challenge name
  startDate: "2026-05-01",      // ← start date
  endDate: "2026-06-30",        // ← end date
  players: [
    { name: "Alice", emoji: "👩🏻", color: "#7C3AED" },
    { name: "Bob",   emoji: "👨🏽", color: "#DB2777" },
    // add up to 6 players
  ],
  stakes: [
    { condition: "Alice wins", result: "Bob buys dinner 🍕" },
  ],
  csvUrl: "PASTE YOUR CSV URL HERE",
  formUrl: "PASTE YOUR FORM URL HERE",
  // ...scoring stays the same unless you want to change it
};
```

Commit and push. GitHub Pages deploys in ~60 seconds.

---

## Step 4 — Install on your phone

Open the URL in **Safari** (iPhone) or **Chrome** (Android):
- iPhone: Share → Add to Home Screen
- Android: Menu → Add to Home Screen

---

## Tip: Ask Claude to help

Not sure how to adapt it? Open the repo in [Claude.ai](https://claude.ai) or [Claude Code](https://github.com/anthropics/claude-code) and say:

> "I forked this challenge tracker PWA. My players are [names], challenge runs [dates], stakes are [X]. Update the CONFIG and the rules sheet to match."

Done in minutes. No coding required.

---

Built with ❤️ by [@camargoarturo](https://linkedin.com/in/camargoarturo)
