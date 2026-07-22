# Offer Comparison Calculator

Compare two job offers side by side, fully in your browser. Base salary, signing bonus, annual bonus, equity, 401k match, benefits, PTO, and commute cost, with a live component-by-component difference table. No server, no tracking, no external dependencies.

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

## Privacy

All client-side. Nothing leaves the browser: no requests, no analytics, no storage. Open the network tab and watch, no traffic.

## License

MIT. Copyright 0xelitesystem 2026.
