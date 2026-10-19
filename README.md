# PingPilot

PingPilot is an internal WhatsApp follow-up supervisor for team/office work: it surfaces pending tasks, unanswered chats, missed follow-ups and commitments due, in one page — before anything is ever sent to anyone.

This repository hosts the **approved internal page design** on GitHub Pages (static hosting).

## ⚠ Sample data only — not live

- Everything on this page is **invented sample data** for design review.
- There is **no Periskope connection yet**, no real WhatsApp chats, no real client/team data, and nothing is sent from this page.
- The "Mark reviewed" controls only change the page on screen.

## What's on the page

- Summary strip: critical alerts, unanswered > 2 hours, pitches awaiting follow-up, commitments due today
- Filter bar on top (team member, role, date, TAT status, waiting time, severity, status, number, search) that drives the alerts, pending tasks and counts together
- Alerts feed with live-ticking waiting timers and TAT pills (On time / Due soon / Overdue)
- Pending tasks list, per-number health, and the follow-up rules in plain English

## How the live version will replace this page

This static GitHub Pages version is design-only. The live version will keep this same design and filters, but:

1. Periskope webhooks will feed PingPilot's own database (read-only pilot: 2 numbers first, only after approval).
2. The page will fetch fresh state every few seconds instead of using built-in sample data.
3. GitHub Pages alone cannot run that backend, so the live page will move to (or be backed by) a small hosted service at that stage. This repo/link may then redirect to the live address.

No secrets, Periskope keys, passwords or real chat data must ever be uploaded to this repository.

## Files

- `index.html` — the self-contained page (no external assets, works offline once loaded)
- `.nojekyll` — tells GitHub Pages to serve files as-is
