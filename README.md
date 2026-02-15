# Expense Tracker

A complete expense tracker web app that runs entirely in your browser with zero cost. Track income and expenses on the fly from any device with local data storage.

## Features

- **Transaction Management**: Add, edit, delete income and expenses with detailed categorization
- **Multiple Accounts**: Track CBA and Westpac accounts separately with real-time balances
- **Budget Tracking**: Set monthly limits per category with progress bars showing % used
- **Debt Tracking**: Monitor debts with payment history and remaining balance calculations
- **Visual Reports**: Category breakdown pie chart and 6-month trend line chart
- **Excel Import/Export**: Import your existing Excel data and export to Excel workbook format
- **JSON Backup**: Export and import complete data backups
- **Mobile Responsive**: Works seamlessly on phone, tablet, and desktop
- **PWA Support**: Install as an app on mobile devices for offline access
- **No Backend**: All data stored locally in IndexedDB - completely free, no server costs

## Deploy to GitHub Pages

### 1. Create repo

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
```

### 2. Push to GitHub

```bash
# Create repo on GitHub.com (click + → New repository → name: expense-tracker)
git remote add origin https://github.com/YOUR_USERNAME/expense-tracker.git
git push -u origin main
```

### 3. Enable GitHub Pages

- Go to repo Settings → Pages
- Source: Deploy from branch
- Branch: main, folder: / (root)
- Save

### 4. Access in 2 minutes at

```
https://YOUR_USERNAME.github.io/expense-tracker
```

## Usage

### Adding Transactions

1. Click the **+** button (bottom right on Transactions tab)
2. Fill in date, description, type (income/expense), amount, category, and account
3. Add optional notes
4. Click **Save**

### Setting Budgets

1. Go to **Budgets** tab
2. Click **Set Budget**
3. Choose category and enter monthly limit
4. Track spending with visual progress bars

### Tracking Debts

1. Go to **Debts** tab
2. Click **Add Debt**
3. Enter debt name and total amount
4. Record payments with the **Pay** button
5. View payment history and remaining balance

### Importing Excel Data

Your existing Excel format is supported:
- Row 0: "CBA" (col 0), "Westpac" (col 6)
- Row 2: Date | Description | Category | Credit | Debit (for each account)
- Row 3+: Transaction data
- Credit = income, Debit = expense
- Rows with "Balance BF" are automatically skipped

**To import:**
1. Go to **Reports** tab
2. Click **Import Excel File**
3. Select your .xlsx file
4. Transactions are imported automatically

### Exporting Data

**Export to Excel:**
- Creates multi-sheet workbook (one sheet per month)
- Matches your original format with CBA and Westpac columns
- Perfect for archiving or external analysis

**Export JSON Backup:**
- Complete backup of all transactions, budgets, and debts
- Use for weekly backups or transferring data between devices
- Import the JSON file on another device to sync data

### Multi-Device Usage

Since data is stored locally per device:
1. Export JSON backup from Device A
2. Download the backup file
3. Transfer file to Device B (email, cloud storage, etc.)
4. Import JSON backup on Device B
5. Repeat weekly to keep devices in sync

### Mobile Installation

When you open the app on mobile, your browser will prompt you to "Add to Home Screen" or "Install App". This enables:
- Offline access
- Full-screen experience
- App icon on home screen
- Works like a native app

## Categories

**Income:** Income

**Expenses:** Groceries, Dining Out, Transport, Fuel, Healthcare, Medication, Entertainment, Shopping, Utilities, Rent, Insurance, Savings, Debt Payment, Other

## Tech Stack

- Vanilla JavaScript (no build step required)
- Tailwind CSS 3.x (via CDN)
- Chart.js 4.x (via CDN)
- SheetJS xlsx 0.18.x (via CDN)
- IndexedDB (native browser storage)

## Data Storage

All data is stored locally in your browser using IndexedDB. This means:
- ✅ Zero cost (no server or database fees)
- ✅ Fast performance (local access)
- ✅ Privacy (data never leaves your device)
- ✅ Works offline
- ⚠️ Data is per device (use JSON export/import to sync)
- ⚠️ Clearing browser data deletes transactions (backup regularly!)

## Browser Support

Works on all modern browsers:
- Chrome 87+
- Firefox 78+
- Safari 14+
- Edge 87+

## Security

- No external API calls (except CDN resources)
- No authentication required
- No personal data transmitted
- All data stays on your device

## Troubleshooting

**Q: My transactions disappeared**
A: Browser data was cleared. Always export JSON backups weekly.

**Q: Import not working**
A: Ensure Excel file matches the format (CBA/Westpac headers in row 0, column headers in row 2).

**Q: Can't see charts**
A: Ensure JavaScript is enabled and you have an internet connection (for CDN resources on first load).

**Q: How do I sync between phone and computer?**
A: Export JSON from one device, transfer the file, and import on the other device.

## License

Free to use and modify for personal use.
