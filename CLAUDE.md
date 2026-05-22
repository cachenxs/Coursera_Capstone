# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Coursera IBM Data Science Professional Certificate Capstone project. It investigates the factors correlated with auto theft in **Toronto** and **Vancouver**, using public crime datasets, Foursquare venue data, and weather records. All work lives in Jupyter notebooks — there is no application code, build system, or test suite.

## Running Notebooks

```bash
jupyter notebook          # launch the notebook server
jupyter nbconvert --to notebook --execute <notebook>.ipynb   # execute a notebook non-interactively
```

## Notebook Progression

The assignments build on each other in this order:

1. **`capstone_assignment_w1.ipynb`** — hello-world stub; confirms pandas/numpy are importable.
2. **`capstone_w3_assignment.ipynb`** — scrapes the Wikipedia Toronto postal code table with `mechanize` + `BeautifulSoup`, merges multi-neighbourhood rows, produces a 103-row `df` with columns `[PostalCode, Borough, Neighbourhood]`.
3. **`capstone_w3_assignment_q2.ipynb`** — extends Q1 by joining the postal-code DataFrame to a geospatial CSV (`https://cocl.us/Geospatial_data`) to add `Latitude`/`Longitude`.
4. **`capstone_w3_assignment_q3.ipynb`** — filters to Toronto-containing boroughs, calls the Foursquare Explore API for each neighbourhood, one-hot-encodes venue categories, runs `KMeans(n_clusters=5)`, and renders a `folium` choropleth map (screenshot saved as `w3q3.png` since GitHub can't render interactive maps).
5. **`Capstone - final assignment.ipynb`** — the main deliverable (71 cells). Pulls Toronto auto-theft records from ArcGIS Open Data and Vancouver records from a local `crimedata_csv_all_years.csv`, filters to 2017–2018, correlates theft timing with weather (local `en_climate_daily_ON_6158355_2017_P1D.csv`), converts Vancouver UTM coordinates to lat/lng with a hand-written `utmToLatLng` function, queries Foursquare for venues near each theft location, and produces ranked bar charts of the top venue categories near theft sites.

## Key Libraries

| Library | Purpose |
|---|---|
| `pandas` / `numpy` | Data manipulation |
| `mechanize` + `BeautifulSoup` | HTML scraping of Wikipedia |
| `geocoder` / `geopy.Nominatim` | Address-to-coordinate lookup (geocoder.google was unreliable; notebooks fall back to the CSV) |
| `sklearn.cluster.KMeans` | Neighbourhood clustering |
| `folium` | Interactive map rendering |
| `requests` | Foursquare REST API calls |
| `matplotlib` | Charts and plots |

## External Data Dependencies

The final notebook relies on files that are **not committed** to the repository:

- `crimedata_csv_all_years.csv` — Vancouver crime data (download from the Vancouver Open Data Portal)
- `en_climate_daily_ON_6158355_2017_P1D.csv` — Environment Canada daily climate for Toronto 2017
- `van_theft_venues.pkl`, `tor_theft_venues1.pkl`, `tor_theft_venues3.pkl` — cached Foursquare API results (pickled DataFrames); cells that call `getNearbyVenues` are left as markdown (not run cells) because the Foursquare API credentials embedded in the notebooks may be expired

## Foursquare API

`CLIENT_ID` and `CLIENT_SECRET` are hardcoded in `capstone_w3_assignment_q3.ipynb` and `Capstone - final assignment.ipynb`. If re-running live API calls, replace those values with valid credentials. The notebooks cache results to `.pkl` files to avoid re-fetching.

## Coordinate System Note

Vancouver crime data uses **UTM Zone 10N** coordinates (columns `X`, `Y`). The notebook converts them to WGS84 lat/lng using a custom `utmToLatLng` math function before mapping or passing to Foursquare.
