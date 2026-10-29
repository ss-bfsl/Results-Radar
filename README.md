# Results Radar

A static Indian-stock earnings tracker interface. The holdings list is saved in local browser storage.

## Run locally

Open `index.html` in a browser. No build step or server is required.

## Publish with GitHub Pages

1. Create a GitHub repository and add `index.html`, `styles.css`, `app.js`, and this README at the repository root.
2. Push the files to the `main` branch.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Open the Pages URL shown in that settings screen. It will be available from any device with internet access.

This site uses relative asset paths and does not need a build pipeline to publish.

## Data status

The current version does not fetch earnings dates, filings, financial results, consensus estimates, news, or prices. Those fields show “Not available”; no sample market figures are included. Stock search currently uses a small built-in list of NSE companies and is not a complete exchange directory. Holdings remain local to the browser and do not sync across devices.

To enable automatic refreshes, connect a backend or scheduled GitHub Actions job to a permitted data provider. GitHub Pages itself serves static files and cannot run a background process. NSE provides public filing/calendar pages, while exchange-grade corporate data feeds are separately licensed. A reliable integration for prices, consensus, historical results, and news needs a provider that explicitly permits those uses; do not put provider secrets in the Pages frontend.
