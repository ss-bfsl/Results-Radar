# Results Radar

Responsive React app for keeping an Indian-equity watchlist. The watchlist saves in browser storage. Market data fields deliberately show “Not available” until a verified data provider is configured.

## Run locally

1. Install Node.js 20 or newer.
2. Run `npm install`.
3. Run `npm run dev` and open the local URL Vite prints.

Create a production bundle with `npm run build`; preview it with `npm run preview`.

## GitHub Pages

The repository includes a GitHub Actions workflow that builds the React app and deploys `dist` to Pages on every push to `main`.

1. In the repository, open **Settings → Pages**.
2. Set **Build and deployment → Source** to **GitHub Actions**.
3. Open **Actions** and wait for **Deploy Results Radar** to finish successfully.
4. The project URL will be `https://ss-bfsl.github.io/Results-Radar/`.

Vite is configured with the repository subpath. GitHub Pages does not run a persistent server; this workflow only builds and publishes the frontend.

## Data status

This project currently does not fetch earnings dates, exchange filings, financial results, consensus, news, sentiment, or share prices. It has a small built-in list of common NSE symbols for watchlist search, not a full NSE/BSE directory. It does not include cross-device sync, scheduled market-data refresh, or alert delivery. No sample market metrics are shown.

Official references: [NSE announcements](https://www.nseindia.com/companies-listing/corporate-filings-announcements), [NSE financial results](https://www.nseindia.com/companies-listing/corporate-filings-financial-results), [NSE event calendar](https://www.nseindia.com/companies-listing/corporate-filings-event-calendar?days=7days). A live integration needs a permitted provider for structured exchange and market data; never place provider secrets in this public frontend.
