# Global Palm Oil Trade Atlas

<a href="https://kangyuetong.github.io/global-palm-trade-map/" target="_blank" rel="noopener noreferrer">🌐 Explore the Interactive Dashboard</a>

Developed an interactive trade analytics dashboard using UN Comtrade data (2020–2024) to examine Indonesia's and Malaysia's palm oil export dependence. Analysed destination-market concentration, shifts in export relationships and potential exposure to changes in international demand. Transformed raw trade statistics into interactive maps, comparative visualisations and research-driven insights.

## Files

- `index.html` — self-contained website. Trade data is embedded; the CSV files are **not required** for the website to run.
- `data/indonesia_palm_oil_exports_2020_2024_clean.csv` — cleaned Indonesia partner-level exports.
- `data/malaysia_palm_oil_exports_2020_2024_clean.csv` — cleaned Malaysia partner-level exports.
- `data/combined_palm_oil_exports_2020_2024_clean.csv` — combined cleaned research dataset.

## Data source and method

Source: UN Comtrade official exports downloaded on 10 November 2026. Annual trade, HS 1511 (palm oil and its fractions), reporters Indonesia and Malaysia, export flow, 2020–2024. The files exclude `World` aggregate partner rows to prevent double-counting in partner rankings. `trade_value_usd` comes from `primaryValue`; `net_weight_tonnes` comes from `netWgt / 1,000` (kilograms to metric tonnes). Missing weight values remain blank, **not zero**. Country names and reported trade values are otherwise retained. No deflation or inflation adjustment was applied.

**Important limitation:** The Indonesia 2024 record for China has a reported trade value but missing `netWgt`, so volume-based rankings/totals must not treat it as zero or assume completeness. The Indonesia 2024 `World` aggregate also lacks `netWgt`. Partner sums may differ from World totals. These are reporter-side export records, not independently verified mirror imports.

The website is a standalone visualization snapshot. Updating CSVs alone will **not** update the embedded dashboard data; `index.html` must also be regenerated.

Official source: https://comtradeplus.un.org/
