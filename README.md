# Stock Price Fetcher 📈

A Streamlit web app to fetch live stock prices from Yahoo Finance for Indian stocks.

## Features

- 📊 Upload CSV or Excel files with stock symbols
- 🎯 Auto-detects symbol columns
- 📈 Fetches live prices from Yahoo Finance
- 💾 Download updated Excel file with prices
- 🔄 Supports both NSE (.NS) and BSE (.BO) exchanges
- ⚡ Configurable delay to avoid rate limiting

## Local Installation

1. Install requirements:
```bash
pip install -r requirements.txt
```

2. Run the app:
```bash
streamlit run streamlit_app.py
```

3. Open browser at `http://localhost:8501`

## Deploy to Streamlit Cloud

### Option 1: Deploy from GitHub

1. **Push code to GitHub:**
   - Create a new repository on GitHub
   - Push these files:
     - `streamlit_app.py`
     - `requirements.txt`
     - `README.md`
     - `default_stocks.csv` (your Nifty 500 list)

2. **Deploy on Streamlit Cloud:**
   - Go to https://share.streamlit.io/
   - Click "New app"
   - Connect your GitHub repository
   - Select `streamlit_app.py` as main file
   - Click "Deploy"

### Option 2: Deploy Directly

1. Go to https://share.streamlit.io/
2. Click "New app"
3. Choose "Paste GitHub URL"
4. Enter your repository URL
5. Click "Deploy"

## Usage

1. **Upload File:** Upload your CSV or Excel file containing stock symbols
2. **Select Column:** Choose which column contains the symbols
3. **Fetch Prices:** Click the button to fetch live prices
4. **Download:** Download the updated Excel file with prices

## File Format

Your file should have at least one column with stock symbols:

| Symbol   | Company Name              | Exchange |
|----------|---------------------------|----------|
| RELIANCE | Reliance Industries       | NSE      |
| TCS      | Tata Consultancy Services | NSE      |
| INFY     | Infosys                   | NSE      |

## Settings

- **Delay between requests:** Adjust to avoid Yahoo Finance rate limiting (default: 0.2 seconds)
- **Default Exchange:** Choose NSE (.NS) or BSE (.BO) as default

## Notes

- Fetching 500 stocks takes approximately 2-3 minutes
- Yahoo Finance may rate limit if requests are too fast
- Some stocks may fail to fetch (marked as 'N/A' or 'Error')

## Support

For issues or questions, please create an issue on GitHub.

## License

MIT License