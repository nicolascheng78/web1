# Trade Tracker & Portfolio Tools

A lightweight single-page web app for tracking trades, portfolio growth, and compounding performance with Supabase (Google login) and charts.

## Features
- Google login via Supabase Auth
- Trade history logging (date elapsed, symbol, entry, exit, size, % gain, annualized gain)
- Portfolio growth chart
- Trade progression calculator
- Compounding calculator
- Optional Yahoo Finance EOD stock chart with daily caching

## Setup

### 1) Create a Supabase project
- Create a new project at https://supabase.com
- Go to **Authentication → Providers** and enable **Google**
- Add redirect URLs:
  - `http://localhost:5173`
  - `http://localhost:5500`
  - Your production domain (if any)

### 2) Create the database table
Run the SQL in `supabase/schema.sql` inside the Supabase SQL editor.

### 3) Configure the app
Open `app.js` and replace these placeholders:
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`

### 4) Run locally
You can use any static server. Example:
```bash
npx serve .
```
Then open the URL shown in the terminal.

## Notes
- Yahoo Finance requests may be blocked by CORS in some environments. If you encounter errors, you can place a small proxy or use another free market data provider.