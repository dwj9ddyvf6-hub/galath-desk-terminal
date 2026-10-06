# FolioTend Paper Desk

Static, auto-updating dashboard for a rules-based **paper-trading** desk (Alpaca paper account, simulated money).
Live page: https://dwj9ddyvf6-hub.github.io/galath-desk-terminal/ (this repository is public and served by GitHub Pages).

`index.html` reloads `data.json` every 60 seconds; `data.json` is regenerated and pushed by a publisher outside this repo
only when the numbers change. The data file is built from an allow-list of fields and secret-scanned before every commit.

What the page shows: account equity and P&L (after the session, on the official last-close basis), holdings and queued orders,
committed dollars against each strategy's dollar budget (new positions are sized at a fixed dollar amount per position),
closed trades, a strategy breakdown and a desk health line. A second **Test** tab shows a separate paper test account the same way.
A third **ChartsLector** tab is a read-only view of publicly published market indicators recomputed from end-of-day data
(VIX Mood Ring, Pulse, Risk Appetite Meter, breadth, an opportunity ranker, theme heatmap and rotation, stock screens) plus research
scorecards for each system (backtest edge, out-of-sample test, status). Its data file `chartslector.json` is rebuilt after the close and
pushed only after an independent recompute check passes. Nothing on that tab is a trading signal for this desk.

What the page never shows: stop levels, targets, planned exits or exit dates, hold lengths, or the rule details behind any strategy.

**Paper trading, not investment advice.**
