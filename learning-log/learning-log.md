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

## Week 2 — 21 April 2026

**Period:** 14–21 April 2026  
**Phase:** Foundation — travel week, lighter pace

### Field observation — La Guajira and the Caribbean coast, Colombia

Spent the week travelling between Santa Marta, Dibulla, and Cartagena. The time in Dibulla and the surrounding La Guajira region was unexpectedly relevant to the direction of this work.

La Guajira sits on the Caribbean coast — high winds, strong waves, intense sun, and intermittent rainfall. It is widely cited as one of the most energy-rich regions in Latin America, with wind and solar potential reportedly sufficient to power all of Colombia twice over. And yet the communities there lack consistent access to food and clean water, rely on cheap oil for electricity, and live in conditions far removed from that potential.

This is a concrete version of the development problem this work is oriented around: the gap between available natural resources and the ability of communities to access and benefit from them. The barriers aren't purely technical — they involve energy company interests, governance, investment, and political economy. Seeing it directly rather than reading about it in a report sharpens the motivation behind the analytical work.

The same dynamic appeared in Cartagena — a city experiencing power cuts during the FICCI film festival, with local shopkeepers describing ongoing outages, in a region sitting next to vast renewable energy sources. If infrastructure gaps affect visible, relatively developed urban settings this acutely, the implications for rural and remote communities are considerably more severe.

*This is not yet connected to the core project methodology, but it is relevant context for understanding why agricultural water management and energy access are interlinked development challenges — particularly in Latin America and SSA.*

### AI course

Chapter 3 · in progress  
*Real World AI* — covering how AI is applied to practical problem-solving. The section on search and problem-solving clicked particularly well: currently playing chess on Duolingo, which almost certainly uses the same kind of decision-tree logic described in the chapter — mapping possible moves as nodes, evaluating paths forward. Seeing the concept in something familiar made the abstraction tangible. Next section: odds and probability.

### Python

Lists · Part 4 of 7  
Working through list operations and manipulation. Expect to complete all 7 parts shortly after returning to Berlin. The next logical step after lists is toward functions and then pandas — the bridge to actual data handling.

*Still to understand: DataFrames and how pandas structures tabular data. This remains the key milestone before touching any real dataset.*

### Domain reading — World Bank *Nourish and Flourish* (continued)

Lighter reading week given the travel. Continued with the report — consolidating the blue/green water framing from week 1 rather than covering significant new ground. The field observations in La Guajira gave some of the earlier statistics a different texture — the report's framing of energy use in irrigation (irrigation responsible for over 15% of agriculture-related greenhouse gas emissions, groundwater pumping accounting for nearly 90% of irrigation's energy use) lands differently after seeing communities running pumps on cheap oil.

### Resources

- World Bank (2025) — *Nourish and Flourish: Water Solutions for a Food-Secure World* — *in progress*

### Next week

- Complete Python lists (parts 5–7)
- Begin moving toward pandas — understand DataFrames properly
- Continue AI course — odds and probability section
- Return to AQUASTAT exploration and World Bank report with more focus back in Berlin

---

## Week 3 — 27 April 2026

**Period:** 22–27 April 2026
**Phase:** Foundation — back in Berlin, pace picking up

### AI course

Machine learning chapter · 13/25 complete · 50% through the course

A significant milestone — halfway. The machine learning chapter is connecting well with the earlier AI foundations. The progression from rule-based systems to learned patterns is starting to feel like a coherent arc rather than separate topics.

### Python — Kaggle

Lists · Section 7 of 7 — final section in progress

Almost through lists. Planning to revisit loops, list comprehension, strings, and dictionaries in more depth before moving on — the instinct to consolidate before advancing is the right one. These concepts (particularly list comprehension and dictionaries) will come up constantly in data handling work later, so it's worth being comfortable with them now.

*Next milestone: pandas and DataFrames — the bridge to real data work.*

### Domain reading — World Bank *Nourish and Flourish* (continued)

Continued with the report alongside some self-directed exploration prompted by longer-standing interest in water and permaculture. Two projects encountered via Andrew Millison (permaculture farmer, YouTube) stood out:

**Riyadh water recycling system** — Riyadh sources water via energy-intensive desalination from the Persian Gulf. Historically this led to significant pollution, sewage, and water quality problems around the city. The response was a nature-based urban water recycling system: oxygen is initially pumped into degraded water bodies to restore them, tree-based marsh areas remove excess nutrients, and the water is cycled repeatedly through the city. Excess water flows downstream for urban farming. A case study in closing the water loop at city scale using ecological methods rather than purely technical infrastructure.

**UN Massive Lake Project — Africa** — a large-scale water harvesting initiative demonstrating receding cultivation: as water levels drop seasonally, farming follows the waterline, using residual moisture stored in reformed land. Land is reshaped to retain and distribute water, keeping basins saturated through the dry season. A low-infrastructure, high-impact approach to food and water security in arid and semi-arid regions.

### Background context worth noting

Interest in water systems and permaculture has been building for 2–3 years — Andrew Millison's work was an early reference point before this career direction had a clear shape. The current transition is partly about finding a professional path into something that was already a genuine area of curiosity. A permaculture design course is on the longer-term horizon as a complement to the analytical and technical work.

This matters for the portfolio framing: the domain interest is not manufactured for career positioning — it has roots.

### Resources

- World Bank (2025) — *Nourish and Flourish: Water Solutions for a Food-Secure World* — *in progress*
- Andrew Millison — Permaculture YouTube channel — [youtube.com/@andrewmillison](https://www.youtube.com/@andrewmillison)
- Riyadh water recycling case study — via Millison
- UN Massive Lake Project — via Millison

### Next week

- Complete Python lists section 7, then consolidate loops, list comprehension, strings, dictionaries
- Begin pandas — DataFrames
- Finish AI course (target: this week)
- Continue World Bank report
- Return to AQUASTAT exploration

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
