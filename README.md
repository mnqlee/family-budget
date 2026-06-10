# 💰 Family Budget

A zero-based "every dollar has a home" budgeting app built for one-income families who budget by bi-weekly pay periods. Live-syncs between devices so both spouses always see the same budget.

**Live app:** https://mnqlee.github.io/family-budget/

---

## How We Use It

1. **Payday (1st and 16th):** Enter the paycheck → tap ⎘ Copy Last → adjust → every dollar assigned until Unassigned = $0.00
2. **During the period:** Log spending as it happens, from either phone
3. **Watch the alerts:** the Budget tab badge lights up if any envelope is in trouble
4. **End of month:** 💑 Monthly Money Meeting checklist together

## Features

| Tab | What's There |
|---|---|
| 📋 Budget | Envelopes by group (Bills / Living / Goals), bill-paid checkboxes, rollover, smart alerts, per-line notes |
| 💳 Spending | Transaction log with person tracking, memos, split transactions, recurring flags |
| 📊 Month | Income/spent/savings rate, category breakdown with 3-month trends, by-person totals |
| 🎯 Goals | Money Meeting checklist, annual expense calendar, sinking funds, savings goals, giving tracker |
| 📉 Debt | Avalanche/snowball payoff strategies with payoff-month estimates |
| 📈 Wealth | Net worth snapshots, Windfall Waterfall allocator |
| 🔮 Planner | Personalized insights, Baby Steps tracker, What-If debt simulator |

## Smart Alerts

- 🚨 **Critical** — envelope over budget
- ⚠️ **Warning** — 90%+ spent
- ⚡ **Watch** — spending faster than the period is passing (25% buffer)
- ✅ **Good** — on pace (within 5–10%)

## Household Sync

- Tap **Sync** → Create New Household on the first device → share the 6-letter code
- Second device: **Sync** → Join Existing Household → enter code
- Changes sync every ~6 seconds via Firebase Realtime Database
- Each device also keeps a full local copy — the app works offline and catches up when back online

## Backup & Restore

Tap **💾** in the header:
- **Export** — downloads a dated JSON file with every piece of data
- **Import** — paste a backup to fully restore

Do an export after every Money Meeting. Takes five seconds.

## Tech Notes

- Single-file React app (no build step) hosted on GitHub Pages
- Sync via Firebase Realtime Database REST API — no SDK, no accounts, no server to maintain
- Local data lives in browser localStorage under `hb4_*` keys
- **Add to Home Screen** on mobile for an app-like experience

## Privacy

This is a personal family tool. Budget data syncs through a private Firebase project owned by us, addressed by household code. No accounts, no analytics, no third parties.
