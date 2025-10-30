# Deepgram Sales Dashboard - Usage Guide

## 🎯 Quick Start for Sales Reps

### First Time Setup

1. **Open** `dashboard.html` in your browser
2. **Clear Demo Data**: Click "🗑️ Clear My Data"
3. **Import Your Data**: Click "📥 Import from Salesforce"
   - Export customer list from Salesforce as CSV
   - Upload or paste the CSV data
   - Click "Import Data"

### Salesforce CSV Export

Required columns (flexible naming):
- Customer Name (or Account Name, Company)
- Location (or State, Country)
- Use Case (or Industry)
- Starting Credits (or Contract Value)
- Credits Remaining (or Balance)
- Start Date
- Contract End Date

## 📊 Dashboard Features

### 👥 Customers Tab
- View all active customers
- Click cells to edit inline
- Track credits, renewals, and contracts
- Yellow highlighting for renewals within 4 months

### 🎯 Prospects Tab
- Track sales pipeline
- Stage management (Lead → Demo → Proposal → Won)
- Convert to customers with ✅ button
- Click "➕ Add Prospect" button in the tab

### ⚡ Concurrency Tab
- **Hosted customers**: View real-time concurrency
- **Self-hosted customers**: Separate table (no usage tracking)
- **Peak Period Selector**: Switch between 24h, 7d, 30d, 90d, All Time
- Color-coded utilization (Red >90%, Yellow >75%, Green <75%)

### 🗺️ Map View
- Geographic distribution of customers
- Color-coded markers by credit status
- Click markers for customer details

### 📈 Usage Trends Tab

#### Customer Filtering
- **Search box**: Type customer name to filter
- **Select All checkbox**: Toggle all customers
- **Alphabetical list**: Easy to scan

#### Interactive Chart
- ✅ **Tooltips disabled** - no hover box
- ✅ **Click any customer line** to see details
- ✅ **Click legend names** to see details

#### Detailed Customer View (Click a Line!)

Shows comprehensive breakdown:

**📊 Summary Stats**
- Total Consumed
- Daily Burn Rate
- Monthly Projected
- Credits Remaining

**🎙️ Speech-to-Text (STT) Breakdown**
- **Streaming** vs **Batch** split
- **Models**: Nova 2, Nova 3, Flux usage

**🔊 Text-to-Speech (TTS) Breakdown**
- **REST API** vs **Streaming** split
- **Models**: Aura 1, Aura 2 usage

**🤖 Voice Agent API Breakdown**
- **LLM Model** usage
- **TTS Model** usage
- **BYO Options** usage

**📈 Historical & Projected Chart**
- Green line: Last 6 months (historical)
- Orange dashed line: Next 6 months (projected with 5% monthly growth)

#### Zero Date Projections
- Shows when customers will run out of credits
- Red border: < 30 days (URGENT!)
- Yellow: 30-90 days
- Green: > 90 days
- Shows daily burn rate

## 🔄 API Integration

### Setup Deepgram API
1. Click "🔑 Set API Key"
2. Enter your Deepgram API key
3. Add Project ID and Balance ID for each customer (click cells to edit)
4. Click 🔄 next to customer to refresh balance
5. Or click "🔄 Refresh All Balances" for bulk update

## 📥 Import/Export

### Export Your Data
- Click "📊 Export CSV"
- Downloads complete customer list
- Includes all fields (concurrency, peaks, etc.)

### Import New Data
- Click "📥 Import from Salesforce"
- Upload CSV or paste data
- Choose to append or replace

## 💡 Pro Tips

### Finding Upsell Opportunities
1. Sort by **% column** (click header)
2. Look for red cells (< 25% remaining)
3. Check **Zero Date Projections** for urgent renewals
4. View **Concurrency tab** for customers hitting limits (>90% utilization)

### Tracking Product Usage
1. Go to **Usage Trends** tab
2. **Click a customer line** on the chart
3. See detailed breakdown by product and model
4. Review projected growth trajectory

### Managing Renewals
1. Yellow rows = renewal within 4 months
2. "RNWL" badge appears next to customer name
3. Sort by **Contract End Date** to see upcoming renewals
4. Update dates by clicking the cell

### Multi-Rep Usage
- Each sales rep can clear and import their own data
- Data stored locally in browser (isolated per user)
- Export before clearing to backup

## 🚀 Keyboard Shortcuts

- **Enter**: Save inline edit
- **Escape**: Cancel inline edit
- **Click column headers**: Sort table
- **Click chart lines**: Detailed customer view

## 🔒 Data Privacy

- All data stored **locally in your browser**
- No data sent to external servers (except Deepgram API)
- API key stored securely in localStorage
- Safe to use with confidential customer data

## 🐛 Troubleshooting

### Data Not Showing
- Hard refresh: **Cmd+Shift+R** (Mac) or **Ctrl+Shift+F5** (Windows)
- Check browser localStorage is enabled

### API Not Working
- Verify API key has correct permissions
- Check Project ID and Balance ID are correct
- Look in browser console (F12) for errors

### Import Failed
- Ensure CSV has header row
- Check column names match guide above
- Try pasting data instead of file upload

## 📞 Questions?

This dashboard is designed for the Deepgram sales team. For questions or feature requests, reach out to your team lead.

---

**Built for Deepgram Sales Team** | Last Updated: Oct 2025

