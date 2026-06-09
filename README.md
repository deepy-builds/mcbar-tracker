# 📚 Mock Bar Review Sprint Tracker

A personal progress tracker for the **2026 Philippine Mock Bar Exams**, built as a single HTML file with cross-device sync via Google Sheets.

---

## What It Does

- Tracks 50-minute study sprints across a 5-week Reverse Study Order (RSO) schedule (June 10 – July 11, 2026)
- Checkmarks save automatically and sync across devices in real time
- Shows overall progress, a per-week breakdown, a daily streak counter, and a countdown to Exam Day 1 (July 8)
- Highlights the next incomplete session so you always know where to pick up
- Lets you attach quick notes to any study session
- Works on both desktop and mobile — installable as a home screen app

---

## Study Schedule

| Phase | Subject | Weight | Dates |
|-------|---------|--------|-------|
| 1 | Remedial Law & Ethics | 25% | June 10–15 |
| 2 | Criminal Law | 10% | June 16–21 |
| 3 | Civil Law & Land Titles | 20% | June 22–27 |
| 4 | Commercial & Tax Law | 20% | June 28 – July 3 |
| 5 | Political & International Law | 15% | July 4–7 |
| — | Mock Exams | — | July 8–10 |

---

## Tech Stack

- **Pure HTML/CSS/JS** — no frameworks, no build step, one file
- **Google Apps Script** — acts as a lightweight REST API for reading and writing progress
- **Google Sheets** — stores progress data as JSON in a single cell
- **GitHub Pages** — hosts the file for free

---

## How Sync Works

```
Browser (index.html)  →  Google Apps Script (Web App)  →  Google Sheet (JSON in A2)
```

On every checkmark or note, the app POSTs the full state to the Apps Script endpoint. On load, it GETs the latest state from the same endpoint — so any device opening the URL picks up exactly where the last one left off.

If the Sheet is unreachable (e.g. offline), the app falls back to `localStorage` automatically.

---

## Running Locally

No setup needed. Just open `index.html` in any browser.

---

## Hosting

Served via **GitHub Pages** at:
```
[https://deepy-builds.github.io/mcbar-tracker/]
```

To add to your phone's home screen: open the URL in your mobile browser → Share → **Add to Home Screen**.

---

## Resetting Progress

Scroll to the bottom of the tracker and tap **"Reset all progress & notes"**. This clears both the local state and the Google Sheet.

---

*Built with love. You've got this 💗*
