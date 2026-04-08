# Irrigation Water Productivity Gaps in Sub-Saharan Africa
### A geospatial analysis for development investment prioritization

---

## The problem

Irrigation infrastructure across Sub-Saharan Africa has received significant development investment over the past two decades — yet yield gaps between actual and potential agricultural output remain stubbornly wide. A core question for development finance institutions and program designers is not simply *where* irrigation exists, but *where it is underperforming relative to its potential* and *why*.

Without spatially explicit, comparable data on water productivity across the region, investment decisions risk targeting areas on the basis of infrastructure availability alone — missing the more important signal of agronomic and management efficiency.

---

## Objective

This project maps irrigation water productivity (IWP) gaps across Sub-Saharan Africa at sub-national scale, identifying regions where the ratio of crop output to water consumed diverges most significantly from its biophysical potential.

The analysis is intended to support:
- Prioritization of agricultural water management (AWM) investments
- Identification of intervention types most likely to close productivity gaps (technology, extension, institutional)
- A replicable methodology that national programs and regional bodies can adapt

---

## Data and methods

**Primary data sources**
- FAO AQUASTAT — irrigated area and water withdrawal by country and sub-basin
- NASA/USGS MODIS via Google Earth Engine — actual evapotranspiration (ETa) and land surface temperature
- FAO crop production statistics — yield data by country and crop type
- GAEZ v4 (FAO/IIASA) — attainable yield potential under rainfed and irrigated conditions

**Analytical approach**

1. Calculate actual IWP at sub-national level: crop yield per unit of ET consumed
2. Estimate potential IWP from GAEZ attainable yield and reference evapotranspiration (ET₀)
3. Derive the productivity gap: the ratio of actual to potential IWP, expressed as a percentage
4. Cluster regions by gap magnitude and likely limiting factor (water availability, soil quality, management)
5. Overlay with existing development program footprints (World Bank, IFAD, USAID) to identify investment blind spots

**Tools:** Python (GeoPandas, Rasterio, Google Earth Engine Python API), QGIS for validation

---

## Status

| Phase | Description | Timeline | Status |
|-------|-------------|----------|--------|
| 1 | Data acquisition and baseline mapping | Months 1–2 | In progress |
| 2 | IWP gap analysis and clustering | Months 3–4 | Planned |
| 3 | Policy brief and investment recommendations | Months 5–6 | Planned |

---

## Expected findings and use

The analysis is expected to show significant intra-regional variation in IWP gaps that is not captured by country-level statistics — consistent with findings from IWMI's comparative research on irrigation performance. The resulting gap map and typology will be presented as a briefing note suitable for a development finance institution program team.

This is not a final research product. It is a working analysis developed as part of a structured self-directed learning programme in geospatial methods for water and agriculture development.

---

## Learning context

This project is being built in parallel with formal study in Python, geospatial analysis, and AI project management. The `learning-log/` folder documents weekly progress, methodological decisions, and domain learning.

The goal is not only analytical output but the development of a transferable methodology and fluency in the tools and concepts used by program officers, water economists, and M&E specialists in the development sector.

---

## Author

**Tim** — Business analyst and product manager transitioning into digital tools and data systems for water and agriculture development. Based between Berlin, London, and Colombia, focused on Sub-Saharan Africa and South Asia program contexts.

[LinkedIn](https://www.linkedin.com/in/timflemmings77/) | [Contact](tim.flemmings.co@gmail.com)

---

*Data sources are publicly available. All code is open for reuse and adaptation. Feedback and collaboration welcome.*
