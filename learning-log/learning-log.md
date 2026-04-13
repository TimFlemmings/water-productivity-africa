# Learning log

Documenting my transition into the water, agriculture, and digital development space — combining AI, Python, and domain knowledge in water economics and geospatial analysis.

**Target roles:** Digital agriculture program officer · Water data specialist · Agri-tech product manager  
**Target organisations:** World Bank · FAO · CGIAR · IWMI · IFC  
**Geographies of focus:** Sub-Saharan Africa · South Asia

---

## Week 1 — 6 April 2026

**Period:** 6 April 2026  
**Phase:** Project setup and orientation

### Setup

- Created GitHub repository and established folder structure for the irrigation water productivity project
- Started AI course (chapters 1–2) as a parallel track alongside domain learning
- Started Python course — foundational track building toward geospatial analysis
- Began structured domain reading — World Bank *Nourish and Flourish* water solutions report

### AI course

Chapter 2 · 4/25 units complete

Covering foundations of intelligence and the philosophy of AI. The framing around what "intelligence" actually means — computationally and philosophically — is connecting with a background in philosophy of mind. Makes the material more intuitive than expected.

### Python

Working through booleans, conditionals, and foundational syntax. Good refresher on logical thinking and the problem-solving patterns that will apply to data work later. Not yet at pandas or the geospatial stack — that's the direction of travel.

*To understand next: what a DataFrame is and how pandas structures tabular data — this will matter when handling AQUASTAT country-level datasets.*

### Domain reading — World Bank *Nourish and Flourish*

Focused on the blue water / green water distinction. Key figures that stood out:

- Of the ~119,000 km³ of annual precipitation falling on land, ~60% becomes green water and ~40% becomes blue water
- Humans withdraw only 3,800–4,000 km³/year — about 9% of available blue water — and use 5–6% for irrigation
- Irrigated land is just 6.5% of total agricultural land, yet produces 40% of global food supply
- Rice yields across 12 SSA countries: 0.6–2.3 t/ha rainfed vs 2.5–5.6 t/ha irrigated

The insight that landed: applying blue water increases the efficacy of green water — lifting productivity per unit of water used so less land and water are needed overall for the same food output. Irrigation reframed as a productivity multiplier, not just a resource cost.

Also noted: only 3% of globally equipped irrigation area is in low-income countries vs 18% in high-income countries. Directly contextualises the development finance case for SSA investment.

### Started exploring — things encountered this week, to understand properly

Curiosity led to initial reading around the project methodology. Not yet understood in depth — these are targets for the coming weeks:

**FAO AQUASTAT** — FAO's global water database with country-level data on irrigated area, water withdrawal, and agricultural water use. Need to explore the database structure and understand what SSA country data is actually available and at what temporal resolution.

**IWMI Water Accounting Plus (WA+)** — a framework that distinguishes between *depleted* water (consumed by crops via evapotranspiration) and *non-depleted* water (returns to the system). Relevant because irrigation water productivity (IWP) sits within this framework. To understand properly: why ET is used as the denominator for IWP rather than water withdrawn or delivered.

**Evapotranspiration (ET) and satellite measurement** — started to understand how MODIS (a satellite) estimates crop water consumption from thermal and reflectance data rather than direct measurement. The concept: crops consuming water stay cooler and more humid, and satellites can work backwards from that thermal signature to estimate actual water use (ETa). To explore further: GEE MODIS ET product documentation.

**Scheme-level data problem** — national and regional databases aggregate data at country level. "Scheme-level" means data at the level of an individual irrigation scheme — a managed area distributing water to farmers. Most databases don't have this, which is why satellite data matters for sub-national analysis. MODIS resolution is 500m per pixel (1 pixel = 25 hectares). To understand: at what point does a scheme become too small for MODIS data to be reliable?

**SPAM (Spatial Production Allocation Model)** — a dataset from IFPRI that disaggregates national crop production statistics down to a ~10km grid. To understand: the methodology uses survey data as inputs but the spatial allocation is modelled — meaning grid-cell estimates carry uncertainty, especially in data-sparse regions like SSA. Need to read the IFPRI technical documentation to understand how much uncertainty to expect.

### Resources

- FAO AQUASTAT — [fao.org/aquastat](https://www.fao.org/aquastat/en/) — *to explore*
- World Bank (2025) — *Nourish and Flourish: Water Solutions for a Food-Secure World* — *in progress*
- IWMI WA+ framework — [wateraccounting.org](http://www.wateraccounting.org/) — *to read*
- GEE MODIS ET dataset documentation — *to read*
- IFPRI SPAM technical documentation — *to read*

### Next week

- Continue AI course — target chapters 3–4
- Continue Python course — begin pandas, understand DataFrames
- Continue World Bank report
- Explore AQUASTAT database — download a small SSA dataset
- Read GEE MODIS ET product documentation
- Read IWMI WA+ framework overview properly
- Begin understanding SPAM methodology via IFPRI documentation

---

## Week 2 — [Date]

**Period:**  
**Phase:**

### AI course

[Chapter · units complete]  
[Key concepts covered]

### Python

[Current section]  
[What clicked or what was hard]

### Domain reading

[Report / paper · source]  
[Key insight or stat]

### Started exploring

[Things encountered this week, to understand properly]

### Resources

-

### Next week

-

---

## Template — copy for each new week

```
## Week N — [Date]

**Period:**  
**Phase:**

### AI course

[Chapter · units complete]  
[Key concepts covered]

### Python

[Current section]  
[What clicked or what was hard]

### Domain reading

[Report / paper · source]  
[Key insight or stat]

### Started exploring

[Things encountered this week, to understand properly — not yet resolved]

### Projects / code

[Link to any scripts or notebooks produced this week]

### Resources

-

### Next week

-
```

---

## Roadmap

| Phase | Timeline | Focus |
|---|---|---|
| Foundation | Months 1–2 | AI course + Python fundamentals |
| Applied Python | Month 2+ | GeoPandas, Rasterio, Google Earth Engine |
| Domain knowledge | Month 2+ | Water economics, development finance, AWM |
| Positioning | Months 4–6 | Junior programs and fellowships — World Bank, CGIAR, IWMI |
| Long-term | Post 6 months | Consultancy track |

---

*Started April 2026*
