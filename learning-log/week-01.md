# Learning log — week 1

**Period:** 6 April 2026
**Phase:** Project setup and orientation

---

## What I did this week

Set up the GitHub repository and folder structure for the irrigation water productivity project. Spent time understanding the conceptual framing — specifically why irrigation water productivity (IWP) is a more useful analytical lens than irrigated area alone for a development finance audience. The distinction matters: a program officer recommending a new irrigation investment needs to know whether the problem is insufficient infrastructure or underperforming existing infrastructure. IWP is the metric that answers that.

Also reviewed the FAO AQUASTAT database structure to understand what country-level data is available and at what temporal resolution. Key finding: AQUASTAT has equipped area and withdrawal data for most SSA countries, but scheme-level data is sparse — which is why the remote sensing layer (GEE/MODIS ETa) is necessary to get sub-national variation.

---

## What I'm learning in Python this week

Focused on foundational Python: data types, control flow, functions. Not yet at the geospatial stack, but beginning to understand how pandas DataFrames work — which will be the backbone of the AQUASTAT data handling later.

One concept that clicked: the idea of a DataFrame as a structured table where each row is an observation and each column is a variable. This maps directly to how AQUASTAT data is organized — one row per country-year, columns for each indicator.

---

## Domain connection I made

Read a summary of the IWMI Water Accounting Plus (WA+) framework this week. The key insight: WA+ distinguishes between *depleted* water (consumed by crops via ET) and *non-depleted* water (returns to the system). IWP analysis sits within this framework — you're measuring how much of the depleted fraction actually ends up as crop output. Understanding this helped me see why evapotranspiration (ET) is the right denominator for IWP, not water withdrawn or water delivered.

This connects directly to why Google Earth Engine's MODIS ET product is a better data source than irrigation withdrawal statistics — withdrawal data captures what enters the scheme, not what crops actually consume.

---

## Questions I'm sitting with

- At what spatial resolution does MODIS ETa data become unreliable for scheme-level analysis? Need to look into this before committing to the methodology.
- How does SPAM allocate crop production spatially — is it modelled or survey-based? This matters for how much I trust the production estimates at grid cell level.
- What is the standard IWP unit used in IWMI/FAO publications? (USD/m³ or kg/m³ — and which crops are benchmarked?)

---

## Resources encountered

- FAO AQUASTAT — [fao.org/aquastat](https://www.fao.org/aquastat/en/)
- Molden et al. (2010) — key reference for IWP conceptual framing
- IWMI WA+ framework overview — [wateraccounting.org](http://www.wateraccounting.org/)
- Google Earth Engine MODIS ET dataset documentation (to read next week)

---

## Next week

- Begin Python pandas exercises using a small AQUASTAT CSV download as practice data
- Read the GEE MODIS ET product documentation and understand the temporal/spatial resolution
- Draft the first notebook skeleton: `01_data_loading.ipynb`
