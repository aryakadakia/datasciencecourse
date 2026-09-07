# Predicting Falcon 9 first stage landings

Capstone project for the IBM Data Science Professional Certificate. The task is
to predict whether the first stage of a SpaceX Falcon 9 launch will land
successfully, which matters commercially because a recovered first stage is the
difference between a launch costing roughly 62 million dollars and 165 million.

The project runs end to end, from collecting the data to serving an interactive
dashboard.

## Pipeline

| Stage | File |
|---|---|
| Collect launch records from the SpaceX REST API | `jupyter-labs-spacex-data-collection-api.ipynb` |
| Scrape historical launch tables from Wikipedia | `jupyter-labs-webscraping.ipynb` |
| Clean and derive the landing outcome label | `labs-jupyter-spacex-Data wrangling.ipynb` |
| Query the dataset in SQL | `sql_spacex_data.ipynb` |
| Exploratory analysis and visualisation | `edadataviz.ipynb` |
| Map launch sites and analyse proximity | `lab_jupyter_launch_site_location.ipynb` |
| Classification models and evaluation | `SpaceX_Machine Learning Prediction_Part_5.ipynb` |
| Interactive dashboard | `spacex_dash_app.py` |

`Data Science Capstone Project.pdf` is the final presentation.

## Notes

The launch site analysis uses Folium to measure distance from each pad to
coastline, railways and highways, which turns out to constrain where pads can be
sited more than the launch profile does.

The dashboard is a Plotly Dash app with a site selector and a payload range
slider, showing success rate by site and the relationship between payload mass
and landing outcome.

Run it with:

```bash
python3 spacex_dash_app.py
```

## Attribution

The lab exercises were provided by IBM Skills Network. The instructional
scaffolding has been removed and what remains is my own code and analysis.
Datasets are loaded from IBM-hosted URLs referenced in the notebooks.

## Stack

`pandas`, `scikit-learn`, `plotly`, `dash`, `folium`, `beautifulsoup4`, `sqlite3`.
