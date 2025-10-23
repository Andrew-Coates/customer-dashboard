# Deepgram Sales Dashboard

A beautiful, interactive dashboard for tracking customer billing and credit consumption using Deepgram's prepaid credit model.

![Dashboard Preview](https://img.shields.io/badge/Status-Production_Ready-success)

## 🎯 Features

### 📊 Customer Management
- **27 Pre-loaded Customers** - Your complete customer base ready to go
- **Inline Editing** - Click any cell to edit customer information
- **Add/Delete Customers** - Full CRUD operations
- **Data Persistence** - All changes saved to browser localStorage
- **Export to CSV** - Download your data anytime

### 💰 Billing & Credits Tracking
- **Real-time Balance Updates** - Fetch live credit data from Deepgram API
- **Color-coded Status Indicators**:
  - 🟢 Green: > 50% credits remaining
  - 🟡 Yellow: 25-50% remaining
  - 🔴 Red: < 25% remaining (upsell opportunity!)
- **Starting Credits vs. Remaining** - Track consumption at a glance
- **Percentage Calculations** - Instant visibility into burn rate

### 🔄 Deepgram API Integration
- **Live Balance Fetching** - Pull real-time credit data using Deepgram Balance API
- **Individual Refresh** - Update one customer at a time
- **Bulk Refresh** - Update all customers with one click
- **Secure API Key Storage** - Stored locally in browser
- **Project ID & Balance ID** - Easy inline editing

### 📈 Analytics & Insights
- **Summary Statistics**:
  - Total Customers
  - Total Contracted Amount
  - Total Credits Remaining
  - At-Risk Customers Count (< 25%)
- **Product Tags** - Visual indicators for:
  - Batch STT
  - Realtime STT
  - Voice Agent API
  - Flux
  - Medical
  - TTS
  - Language Expansion

### 🔍 Sortable Columns
- Click any column header to sort
- Visual indicators (▲/▼) show sort direction
- Smart sorting by data type (text, numbers, dates, percentages)

## 🚀 Quick Start

### Installation
1. Download `dashboard.html`
2. Double-click to open in your browser
3. That's it! No server or dependencies required.

### Setting Up API Integration

1. **Get Your Deepgram API Key**
   - Log into [Deepgram Console](https://console.deepgram.com)
   - Generate an API key

2. **Configure Dashboard**
   - Click **🔑 Set API Key** button
   - Paste your Deepgram API key
   - Click Save

3. **Add Customer IDs**
   - Click on **Project ID** cell for a customer
   - Paste the Deepgram project ID
   - Click on **Balance ID** cell
   - Paste the balance ID
   - Press Enter to save

4. **Refresh Balances**
   - Click **🔄** next to individual customers
   - Or click **🔄 Refresh All Balances** for bulk update

## 📋 Usage

### Editing Data
- **Click any cell** to edit (customer name, location, credits, notes, etc.)
- **Press Enter** to save changes
- **Press Escape** to cancel editing
- All changes auto-save to localStorage

### Managing Customers
- **Add Customer**: Click ➕ button, edit inline
- **Delete Customer**: Click 🗑️ button
- **Sort**: Click column headers
- **Export**: Click 📊 Export CSV

### API Operations
- Individual customer refresh: Click 🔄 in row
- Bulk refresh: Click main **🔄 Refresh All Balances** button
- Status indicators show: Loading → Success/Error

## 🔧 Technical Details

### API Endpoint
```
GET https://api.deepgram.com/v1/projects/{project_id}/balances/{balance_id}
```

### Authentication
```javascript
Authorization: Token {your_api_key}
```

### Response Format
```json
{
  "balance_id": "string",
  "amount": 0,
  "units": "USD",
  "purchase_order_id": "string"
}
```

### Data Storage
- Customer data: `localStorage.deepgramCustomers`
- API key: `localStorage.deepgramApiKey`
- All data stored locally in browser (never sent to third parties)

## 📊 Customer Fields

| Field | Type | Editable | API-Linked |
|-------|------|----------|------------|
| Customer Name | Text | ✅ | - |
| Location | Text | ✅ | - |
| Use Case | Dropdown | ✅ | - |
| Products | Tags | - | - |
| Whitespace | Text | ✅ | - |
| Project ID | Text | ✅ | ✅ |
| Balance ID | Text | ✅ | ✅ |
| Start Date | Date | ✅ | - |
| Starting Credits | Number | ✅ | - |
| Credits Remaining | Number | ✅ | ✅ (API updates) |
| Percentage | Calculated | - | Auto-calculated |
| Notes | Text | ✅ | - |

## 🎨 Use Cases

### Sales Operations
- Track customer consumption in real-time
- Identify upsell opportunities (low credit customers)
- Monitor customer health by credit percentage

### Customer Success
- Proactive outreach before credits run out
- Track usage patterns by product type
- Manage whitespace opportunities

### Finance
- Monitor contracted vs. remaining balances
- Track total exposure across customer base
- Export data for reporting

## 🔒 Security

- API keys stored in browser localStorage only
- No data transmitted to third parties
- Direct communication with Deepgram API only
- HTTPS for all API requests

## 📝 Product Types Supported

- **Batch STT** - Batch speech-to-text processing
- **Realtime STT** - Real-time speech-to-text
- **Voice Agent API** - Conversational voice agents
- **Flux** - Conversational speech recognition
- **Medical** - Medical transcription models
- **TTS** - Text-to-speech
- **Language Expansion** - Multi-language support

## 🤝 Contributing

This dashboard is a single-file HTML application designed for ease of use and portability. Feel free to:
- Customize styles
- Add new features
- Integrate additional Deepgram APIs

## 📚 Resources

- [Deepgram API Documentation](https://developers.deepgram.com/reference)
- [Balance API Reference](https://developers.deepgram.com/reference/manage/billing/get)
- [Deepgram Console](https://console.deepgram.com)

## 🐛 Troubleshooting

### API Key Issues
- Ensure key has proper permissions in Deepgram Console
- Check that key hasn't been revoked
- Verify key format: should be alphanumeric string

### Balance Refresh Fails
- Verify Project ID is correct
- Verify Balance ID is correct
- Check browser console for error messages
- Ensure API key is saved

### Data Not Persisting
- Check browser localStorage is enabled
- Try different browser if issues persist
- Export to CSV as backup

## 📄 License

Copyright © 2025. For internal use.

## 🙏 Acknowledgments

Built for sales operations tracking with Deepgram's powerful speech AI platform.

---

**Made with ❤️ for the Deepgram Sales Team**

