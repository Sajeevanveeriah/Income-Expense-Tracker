# Income & Expense Tracker (GitHub Pages Ready)

Single-page web app (no build step) using Vanilla JS + IndexedDB + Tailwind + Chart.js + SheetJS.

## Files
- `index.html` - complete app
- `.nojekyll` - disables Jekyll processing on GitHub Pages
- `manifest.json` - PWA metadata

## Deploy
```bash
git init
git add .
git commit -m "Expense tracker"
git branch -M main
git remote add origin https://github.com/USERNAME/expense-tracker.git
git push -u origin main
# Enable GitHub Pages: Settings → Pages → main branch → Save
# Access: https://USERNAME.github.io/expense-tracker
```

## What it supports
- Dashboard with current-month income/expense/net, category pie chart, 6-month trend chart.
- Transactions with filters, add/edit/delete, pagination (100/page), debounced search, virtualized rendering behavior for large lists.
- Budgets with green/yellow/red progress bars.
- Debts with add payment and payment history.
- Fixed Costs import and display.
- Excel import in the specified sheet format (monthly sheets + Track + Debt + Fixed Costs).
- Excel export that recreates monthly account-column structure.
- JSON backup export/import.
- IndexedDB stores: `transactions`, `budgets`, `debts`, `fixedCosts`, `settings`.
- Offline-capable PWA install metadata.

## Notes
- Data is local to the browser profile.
- Export JSON backup regularly for portability.
