# 🌱 AgriSmart – Smart Farming for a Sustainable Future

A multilingual (Tamil, English, Malayalam, Hindi, Telugu), mobile-friendly decision-support web app for farmers.
It uses **real NASA POWER data** for the farm's exact location, reads **soil sensor** values (pH, moisture, NPK),
and suggests three crop rotation strategies. Built by **Team ELECTRO** for the NASA Space Apps Challenge 2026 (Coimbatore).

> Powered by NASA Earth Observation Data · Smart Farming | Healthy Soil | Better Future

## Features
- **Page 1 – Farm details:** location, farm size, crops (current crop is optional), soil, water, priorities.
- **Page 2 – NASA data:** live GPS (only after pressing *Use My Location*) or a map pin → daily temperature, rainfall, humidity, solar radiation and soil wetness for 10/15/20 days, graphs and plain-language insights.
- **Soil sensor input:** Bluetooth, USB serial, or pasted reading (`ph=6.5,moist=30,N=40,P=20,K=150`).
- **Page 3 – Rotation plan:** 3 strategies, comparison table, reasons, benefits and risks, information gaps, action plan, read-aloud, PDF (print) and save.
- Language choice is kept on every page.

## Run locally
No build step. Open `index.html` in Chrome or Edge (internet required).

## Deploy on GitHub Pages
1. Create a repository and upload `index.html` and `README.md`.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.
3. Open `https://<your-username>.github.io/<repo-name>/`.

## Tech stack
- Frontend: HTML, CSS, vanilla JavaScript, [Leaflet](https://leafletjs.com) + OpenStreetMap, SVG charts.
- Data/services (no custom backend): [NASA POWER API](https://power.larc.nasa.gov/docs/), OpenStreetMap Nominatim.
- Browser APIs: Geolocation, Web Bluetooth, Web Serial, Web Speech, localStorage, print.

## Data honesty
- Only NASA POWER is fetched live. Soil wetness is a model product, not SMAP; elevation is POWER's grid value, not SRTM.
- GPM, SMAP, MODIS, ECOSTRESS and SRTM need NASA Earthdata login (a backend). They are shown as **Unavailable**, never estimated.
- Recommendations are rule-based and qualitative (High / Medium / Low / Insufficient Data). No yield, income or exact water-saving claims.
- 10–20 days of data is recent weather, not a climate trend.

## Known limitations
- Menus, forms and Page 2 buttons are translated in all five languages; long explanations on Pages 2–3 are mostly English.
- Sensor connection has not been tested with physical hardware. Bluetooth expects the Nordic UART service; USB expects 9600 baud text lines.
- Needs an internet connection.

## Team ELECTRO
Karthik Saran · Harish Kumar · Menaka · Harshaja

## Disclaimer
AgriSmart provides decision-support information based on available environmental and agricultural data. Recommendations are exploratory and should be reviewed with local agricultural experts. Final farming decisions remain with the farmer.
