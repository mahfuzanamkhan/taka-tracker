# 💸 Taka Tracker · টাকা ট্র্যাকার

**Every taka, accounted for. প্রতিটি টাকার হিসাব।**

A zero-dependency, bilingual expense tracker built for how money actually moves in Bangladesh: bKash on Monday, bazar on Friday, Dhar whenever a friend needs it. One HTML file. No framework. No server. No account.

![HTML5](https://img.shields.io/badge/HTML5-vanilla-e34f26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?logo=javascript&logoColor=black)
![Dependencies](https://img.shields.io/badge/dependencies-0-006a4e)
![Hosting](https://img.shields.io/badge/GitHub%20Pages-ready-222?logo=github)
![License](https://img.shields.io/badge/license-MIT-f42a41)

**🔗 Live demo:** `https://mahfuzanamkhan.github.io/taka-tracker/`

---

## Why this exists

Most expense apps are built around credit cards, dollars and Western habits. Taka Tracker starts from the other end: mobile wallets, cash, lakh-and-crore grouping, Eid salami, zakat and the informal Pawna/Dena ledger every family runs in their head.

## Features

### 🇧🇩 Made for Bangladesh
- **Taka-first formatting**: ৳ with lakh/crore grouping (`৳1,25,000`), with optional Bangla digits (`৳১,২৫,০০০`)
- **Full English / বাংলা toggle**: the whole interface switches in one tap
- **Six wallets with live balances**: Cash, bKash, Nagad, Rocket, Bank and Card
- **Local categories**: Bazar, Food & tea, Transport, House rent, Gas-power-water bills, Mobile & internet, Education, Health, Family & remittance, Zakat & charity, Shopping, Fun & outings, Other
- **Local income sources**: Salary, Business, Freelance, Remittance, Gift / Eid salami, Other
- **Dhar ledger**: track *Pawna* (owed to you) and *Dena* (you owe) with partial settlement, progress bars, due dates and notes
- **Zakat calculator**: 2.5% on net wealth once you cross the nisab you enter, pre-filled from your wallet balances

### 📊 Overview
- Total balance across all wallets, with income and spending for the month
- Wallet strip showing each balance at a glance
- Category donut chart and daily spending bar chart, both hand-drawn in SVG
- Auto-generated insights: biggest drain, daily average, month-end projection, savings rate and over-budget warnings
- Month-by-month navigation

### 📒 Ledger
- Add, edit and delete income and expense entries with category, wallet, date and note
- Entries grouped by day
- Live search plus filters by type and wallet

### 🎯 Budgets and goals
- An overall monthly spending cap plus a limit for every category
- Progress bars that turn amber at 80% and red when you cross the line
- Savings goals (Eid fund, laptop, flat deposit) with one-tap +৳500 / +৳1,000 / +৳5,000 top-ups

### 🔒 Privacy and polish
- **Hide balances** toggle for when someone is looking over your shoulder
- Light, dark and auto themes
- Mobile-first layout with a bottom tab bar, thumb-reach add button and safe-area support
- **Backup and restore**: export JSON or CSV, restore from pasted JSON
- Built-in demo data so you can explore in one click

## Your data stays yours

Everything lives in your browser's `localStorage`. There is no backend, no sign-up, no analytics and no tracking. The only network request is the Google Fonts stylesheet, and the app falls back to system fonts without it.

Data is per device and per browser. Use **Tools → Backup & restore** to move it between devices, and clear-site-data will erase it, so export now and then.

## Deploy on GitHub Pages in 2 minutes

1. Create a new repository named `taka-tracker`.
2. Add the file as `index.html` in the repository root.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. Your app goes live at `https://YOUR_USERNAME.github.io/taka-tracker/`.

Prefer to run it locally? Double-click `index.html`. That's the whole setup.

## Under the hood

| Concern | Approach |
|---|---|
| Framework | None. Vanilla JavaScript with template-string rendering |
| State | One object, persisted to `localStorage` |
| Events | Single delegated click handler via `data-a` attributes |
| Charts | Hand-rolled SVG donut and bar chart |
| Numbers | `Intl.NumberFormat` with `en-IN` and `bn-BD` locales |
| Theming | CSS custom properties with `prefers-color-scheme` support |
| Typography | Hind Siliguri and Space Grotesk, with system fallbacks |

## Roadmap

- [ ] Wallet-to-wallet transfers (bKash → Bank, cash-out and the like)
- [ ] App-lock PIN
- [ ] Recurring entries for rent, bills and tuition
- [ ] Installable offline PWA
- [ ] Optional encrypted cross-device sync

## Contributing

Ideas, bug reports and pull requests are welcome. Please keep the project's one rule: **no frameworks, no build step, one self-contained file.**

## License

MIT. Use it, fork it, ship it.

---

<p align="center">Made for Bangladesh. If it saves you a single wasted taka, drop a ⭐</p>
