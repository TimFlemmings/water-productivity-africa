# Data sources

Raw data files are not committed to this repository (see .gitignore) due to file size. This file documents what belongs in each folder and where to obtain it.

---

## data/raw/

Source data, downloaded exactly as provided — never modified.

| File | Source | URL | Notes |
|------|--------|-----|-------|
| AQUASTAT country data | FAO | https://www.fao.org/aquastat/en/databases/ | Download as CSV |
| MODIS ET (MOD16A2) | NASA via GEE | Google Earth Engine | Pulled via GEE Python API |
| GAEZ attainable yield | FAO/IIASA | https://gaez.fao.org/ | Register for access |
| Admin boundaries (SSA) | GADM | https://gadm.org/download_world.html | Level 1 (province) |

---

## data/processed/

Outputs from notebooks — cleaned, merged, and analysis-ready datasets.

Files here are derived from raw sources and documented in the notebooks that produced them.
