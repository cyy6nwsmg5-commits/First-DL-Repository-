# Retirement Dashboard

A self-contained, single-file retirement planning dashboard. No build step, no
dependencies, no backend — just open `index.html` in a browser.

## What it does

- **Savings growth projection** — projects your retirement account balance
  year by year using your current savings, monthly contribution, and expected
  annual return, in both nominal and inflation-adjusted ("today's $") terms.
- **Retirement readiness** — estimates your monthly/annual retirement income
  using a configurable safe withdrawal rate (4% by default) and compares it
  against your stated income goal.
- **Scenario comparison** — compares three plans side by side on the same
  chart and in a summary table:
  - **Current Plan** — your inputs as entered
  - **Save More** — current plan plus an extra monthly contribution
  - **Retire Later** — current plan worked for extra years before retiring
- **Additional accounts & income, each with its own on/off toggle** — so you
  can model what-if scenarios without deleting numbers:
  - Roth IRA, brokerage account, and vested/unvested private equity — folded
    into your invested savings and grown at the same expected return
  - VA disability and military pension (monthly amounts) — added directly to
    your estimated retirement income, in today's dollars
  - Home value — shown as net worth (assumed to track inflation), not counted
    toward retirement income
- **Annual salary & bonus** — used to compute an income-replacement ratio
  (estimated retirement income vs. current total pay)

All inputs update every chart, stat tile, and table live.

## Usage

Open `index.html` directly in any modern browser:

```
open index.html          # macOS
xdg-open index.html      # Linux
```

Or serve it locally:

```
python3 -m http.server 8000
# then visit http://localhost:8000/retirement-dashboard/
```

## Notes

This is a planning estimate, not financial advice. Projections assume a
constant annual return and inflation rate, and do not account for taxes,
fees, employer matching, or Social Security.
