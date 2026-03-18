# cloud-watchlist-scheduler

This repo is a dedicated cloud scheduler for `morrisma666/watchlist-daily-alerts`.

It exists because the private repo's native GitHub `schedule` trigger did not fire
reliably. This scheduler runs on a separate repo and dispatches the production
workflow in the private repo at the target US market time.

Production target:

- US trading days
- 18:45 America/New_York

Required repo secret:

- `TARGET_PAT`
  - A GitHub token that can dispatch workflows in
    `morrisma666/watchlist-daily-alerts`
