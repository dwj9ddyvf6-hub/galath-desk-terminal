# FolioTend Paper Desk

Static, auto-updating dashboard for a rules-based **paper-trading** desk (Alpaca paper account, simulated money).
`index.html` reloads `data.json` every 60 seconds; `data.json` is regenerated and pushed by a publisher outside this repo
only when the numbers change. The data file is built from an allow-list of fields and secret-scanned before every commit.

**Paper trading, not investment advice.**
