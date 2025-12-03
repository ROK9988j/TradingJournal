# Trading Journal Web App

A modern web-based trading journal with AI-powered entry formatting, real-time market data, and TradingView charts.

## Features

- **AI-Powered Journal Entries**: Uses Claude AI to transform your trading thoughts into structured, professional journal entries
- **Real-Time Market Data**: Live prices for SPX, NDX, RUT, DJI, Gold, Bitcoin, TLT, and VIX
- **TradingView Chart**: Embedded SPY chart with snapshot capability
- **Multi-User Support**: Multiple users can have separate journals with invite code registration
- **Cloud Deployment**: Runs on Render.com with persistent JSON storage
- **Image Uploads**: Capture and store chart snapshots via Cloudinary

## Live Demo

https://tradingjournal-t3vl.onrender.com

## Tech Stack

- **Backend**: Python/Flask
- **AI**: Anthropic Claude API
- **Market Data**: yfinance
- **Charts**: TradingView Widget
- **Image Storage**: Cloudinary
- **Hosting**: Render.com

## Environment Variables

Set these in your Render dashboard or `.env` file:

| Variable | Required | Description |
|----------|----------|-------------|
| `IS_CLOUD` | Yes | Set to `true` for cloud deployment |
| `ANTHROPIC_API_KEY` | Yes | Your Claude API key |
| `CLOUDINARY_CLOUD_NAME` | Yes | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Yes | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Yes | Cloudinary API secret |
| `INVITE_CODE` | Optional | Enable multi-user mode with registration code |
| `SECRET_KEY` | Optional | Flask session secret (auto-generated if not set) |

## Local Development

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Copy `.env.example` to `.env` and fill in your API keys
5. Run the app:
   ```bash
   python app.py
   ```
6. Open http://localhost:5000

## Deployment to Render

1. Push code to GitHub
2. Create a new Web Service on Render
3. Connect your GitHub repository
4. Set environment variables in Render dashboard
5. Deploy

## Usage

1. **Register**: Enter invite code and create username/password
2. **Login**: Use your credentials to access your journal
3. **Create Entry**: Type your trading thoughts in the text area
4. **Process with AI**: Click "Process Entry" to format with Claude
5. **Save**: Click "Save to Journal" to store your entry
6. **View History**: Click "Load Previous Entries" to see past entries

## File Structure

```
TradingJournalWeb/
├── app.py              # Main Flask application
├── requirements.txt    # Python dependencies
├── .env.example        # Environment variable template
├── templates/
│   ├── index.html      # Main app interface
│   ├── login.html      # Login page
│   └── register.html   # Registration page
└── README.md           # This file
```

## License

Private use only.
