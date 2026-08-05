<div align="center">

<img src="readme-icon.svg" alt="Crypto Screener Icon" width="300"/>

</div>

# Live Market Screener

Real-time crypto market screener pulling live ticker data directly from **Delta Exchange** via WebSocket. Track 150+ trading pairs with live prices, 24h high/low/volume, sparkline charts, price alerts and a personal watchlist.

**Live Demo:** [https://crypto-stock-scanner.vercel.app/](https://crypto-stock-scanner.vercel.app/)

## Features

- **150+ Crypto Pairs** - BTC, ETH, SOL, DOGE, and many more
- **Real-Time WebSocket Data** - Low-latency streaming from Delta Exchange public API with auto-reconnect
- **Live Price Updates** - Flash animations on price changes with directional colors
- **24h Data Columns** - Change %, 24h High, 24h Low and 24h Volume (USD)
- **Sortable Columns** - Click any column header to sort (price, change, high, low, volume, pair)
- **Market Tabs** - All / Gainers / Losers / Volatile (5%+) / Watchlist
- **Market Overview Bar** - Gainers vs losers counts, best & worst mover, average 24h change
- **Live Sparklines** - Mini price trend charts updated in real-time for every pair
- **Watchlist** - Star your favorite pairs (saved in your browser)
- **Price Alerts** - Set a target price per pair and get a browser notification when crossed
- **Smart Search** - Filter pairs instantly by typing symbol names
- **Export to CSV** - Download the current view as a spreadsheet
- **Dark Theme UI** - Trading-grade dark interface with sticky headers and custom scrollbar
- **Affiliate Integration** - One-click "Trade" link to Delta Exchange (uses your affiliate code)

## Monetization

The site includes several ways to earn:

- **Affiliate links** - Every "Trade" button links to Delta Exchange with your affiliate code (`STJSWZ`). Update it in `index.html` under `myAffiliateCode`.
- **Banner ads (popcash)** - The same working ad script is duplicated in 3 slots: top of the page, above the table, and below the table. Each slot sets `atOptions` right before its own `invoke.js` call so all three run independently. To use a different key or network, update the three script blocks (marked `AD SLOT #1 / #2 / #3`).

## How It Works

1. On load, the screener subscribes to the `ticker` channel on the Delta Exchange public WebSocket endpoint and automatically reconnects if the connection drops.
2. Price ticks are received in real-time and updated directly in the DOM using a cached element system for max performance.
3. Each tick updates the mark price, 24h change, 24h high/low (from the message OHLC), 24h volume and appends to the pair's sparkline history.
4. Positive changes are highlighted in green; negative changes in red.
5. The live status indicator pulses while the connection is active.

## Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript (no frameworks)
- **Data Source:** [Delta Exchange](https://www.delta.exchange) public WebSocket API
- **Deployment:** Vercel

## Files

- `index.html` - Complete single-file application (HTML + CSS + JS)

## License

Open source and free to use.
