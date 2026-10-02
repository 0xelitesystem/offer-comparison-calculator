# Offer Comparison Calculator

Compare two job offers side by side, fully in your browser. Base salary, signing bonus, annual bonus, equity, 401k match, benefits, PTO, and commute cost, with a live component-by-component difference table. No server, no tracking, no external dependencies.

**Live demo:** https://0xelitesystem.github.io/offer-comparison-calculator/

For general information only. This is not financial, tax or legal advice. Check the numbers with a qualified professional before you rely on them.

## Live demo

https://0xelitesystem.github.io/offer-comparison-calculator/

## Features

- Two offer cards with the full comp picture: base, one-time signing bonus, annual bonus (% of base or flat), estimated equity grant value over 4 years, 401k match (match % up to a % of salary), other annual benefits value, PTO days, remote/hybrid/onsite, and optional monthly commute cost
- Year-1 total comp and average annual comp over a 1 to 4 year horizon slider (signing bonus is amortized across the horizon)
- Clean side-by-side table with a difference column for every component
- Cost-of-living free-text note plus an optional user-supplied COL adjustment percent per offer, shown as a clearly labeled adjusted line
- PTO days shown for comparison but honestly not converted to dollars
- Copy-as-text summary button for pasting into notes or a message
- Light and dark theme, keyboard friendly, works offline

## How it works

Everything is arithmetic on your inputs, recalculated live:

- Annual bonus = base x percent, or the flat amount you enter
- Equity per year = your estimated 4-year grant value divided by 4. The tool says this plainly: private-company equity value is speculative and may be worth zero
- 401k match per year = base x match % x cap %, assuming you contribute enough to capture the full match
- Commute cost x 12 is subtracted from effective comp
- Year-1 total = base + signing + bonus + equity/yr + match + benefits - commute
- Average annual over N years = the same, but with signing divided by N

There is no market data, no benchmarks, and nothing fetched. Every number is yours.

## Use

1. Fill in each offer card: base salary, signing bonus, annual bonus, equity estimate, 401k match, benefits value, PTO days, work setup, and commute cost.
2. Set the horizon slider from 1 to 4 years to spread the signing bonus.
3. Read the side-by-side table and the difference column for each component.
4. Click Copy summary as text to paste the comparison into notes or a message.

## Why this exists

Comparing offers means putting salary, bonus, equity, and benefits figures somewhere, and most online comparison tools are lead-generation pages. This is one HTML file that does the arithmetic in your browser with no tracking and no network calls. MIT licensed, so you can check every formula.

## Privacy

All client-side. Nothing leaves the browser: no requests, no analytics, no storage of anything you enter. The only thing the page writes to your browser is your light or dark theme choice, saved in localStorage under the key `theme` when you press the theme button, so the page opens in the same theme next time. Clear site data to remove it. Open the network tab and watch, no traffic.

## Run locally

```
git clone https://github.com/0xelitesystem/offer-comparison-calculator
cd offer-comparison-calculator
```

Then open `index.html` in any browser. Or serve the folder with `python -m http.server` and visit http://localhost:8000.

## Build

No build step. The whole tool is one file, `index.html`, with its CSS and JavaScript inline.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
