# County Climate Analysis — Final

This repository contains data pulling, processing, and visualization work for county-level climate analysis in California (temperature, percipitation and wind). We used data from NCEI and Open-Meteo and have included our notebooks, CSV outputs and visualizations.

## Contents

- `Data Pulling NCEI-Open Meteo/`
  - `Final_NCEI Data_Pulling.ipynb` — Notebook to pull/process climate data from NCEI.
  - `Final_OpenMeteo_Data_Pulling.ipynb` — Notebook to pull/process climate data from Open-Meteo.
- `CSV/`
  - `seasonal_summary_temp_celsius.csv` — Processed seasonal temperature summary (°C). (NCEI)
  - `seasonal_summary_temp_fahrenheit.csv` — Processed seasonal temperature summary (°F). (NCEI)
  - `seasonal_summary_wind_full.csv` — Processed seasonal wind summary (OpenMeteo).
- `Visualizations/`
  - `climate_visualizations.ipynb` — Notebook with climate related visualizations
  - `folium_map.ipynb` — Notebook with code for folium map
  - `california_climate_map.html` — Interactive folium map

## Project overview

Our project goal is to pull climate data from public APIs  we specifically used NCEI and Open-Meteo, and then aggregate it by season and county, and create CSV summaries and visualizations. This repo provides notebooks for the data collection, cleaning, aggregation, and visualization process so you can reproduce or extend the analysis.

## Quick start (macOS, zsh)

1. Clone or open this workspace into VS Code.
2. Create and activate a Python virtual environment (recommended):

```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Install core packages (suggested):

```bash
pip install --upgrade pip
pip install pandas numpy requests jupyterlab matplotlib folium geopandas
```

Note: If your environment lacks system dependencies for `geopandas`, follow geopandas install instructions for macOS (conda is easiest) or install required system libs via Homebrew.

4. Launch Jupyter Lab / Notebook and open the notebooks:

```bash
jupyter lab
# or
jupyter notebook
```

Open and run:
- `Data Pulling NCEI-Open Meteo/Final_NCEI Data_Pulling.ipynb`
- `Data Pulling NCEI-Open Meteo/Final_OpenMeteo_Data_Pulling.ipynb`
- `Visualizations/climate_visualizations.ipynb` and `Visualizations/folium_map.ipynb`

Running the first two notebooks will (re)generate the CSV files in `CSV/`.

## Reproducibility and notes

- The NCEI API requires a token to use the API as well as has a rate limit on requests, so take that into consideration when using this repo.
- The Open-Meteo API is typically free to call without a key.
- Some of the notebooks provided may save large intermediate files or take time to run.

## File structure (summary)

- `Data Pulling NCEI-Open Meteo/` — Notebooks that pull and process raw data.
- `CSV/` — CSV outputs (seasonal summaries) used by visualizations.
- `Visualizations/` — Notebooks and an exported HTML map for visual analysis.


