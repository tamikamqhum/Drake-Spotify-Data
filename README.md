# Drake Spotify Data — Project README

## Dataset content

- Source file: `/mnt/data/drake.data.csv`

- Columns detected:

  - `artist_name` — type: object, missing: 0, unique: 1

  - `artist_id` — type: object, missing: 0, unique: 1

  - `album_id` — type: object, missing: 0, unique: 39

  - `album_type` — type: object, missing: 0, unique: 1

  - `album_release_date` — type: object, missing: 0, unique: 19

  - `album_release_year` — type: int64, missing: 0, unique: 12

  - `album_release_date_precision` — type: object, missing: 0, unique: 2

  - `danceability` — type: float64, missing: 0, unique: 345

  - `energy` — type: float64, missing: 0, unique: 358

  - `key` — type: int64, missing: 0, unique: 12

  - `loudness` — type: float64, missing: 0, unique: 511

  - `mode` — type: int64, missing: 0, unique: 2

  - `speechiness` — type: float64, missing: 0, unique: 386

  - `acousticness` — type: float64, missing: 0, unique: 446

  - `instrumentalness` — type: float64, missing: 0, unique: 245

  - `liveness` — type: float64, missing: 0, unique: 278

  - `valence` — type: float64, missing: 0, unique: 385

  - `tempo` — type: float64, missing: 0, unique: 539

  - `track_id` — type: object, missing: 0, unique: 662

  - `analysis_url` — type: object, missing: 0, unique: 662

  - `time_signature` — type: int64, missing: 0, unique: 4

  - `disc_number` — type: int64, missing: 0, unique: 2

  - `duration_ms` — type: int64, missing: 0, unique: 355

  - `explicit` — type: bool, missing: 0, unique: 2

  - `track_href` — type: object, missing: 0, unique: 662

  - `is_local` — type: bool, missing: 0, unique: 1

  - `track_name` — type: object, missing: 0, unique: 247

  - `track_preview_url` — type: float64, missing: 662, unique: 1

  - `track_number` — type: int64, missing: 0, unique: 22

  - `type` — type: object, missing: 0, unique: 1

  - `track_uri` — type: object, missing: 0, unique: 662

  - `external_urls.spotify` — type: object, missing: 0, unique: 662

  - `album_name` — type: object, missing: 0, unique: 18

  - `key_name` — type: object, missing: 0, unique: 12

  - `mode_name` — type: object, missing: 0, unique: 2

  - `key_mode` — type: object, missing: 0, unique: 24


## Business requirements

- Provide insights about Drake's tracks and streaming behavior.
- Build a dashboard for stakeholders to explore track-level metrics and trends.
- Enable simple predictive modeling for future stream counts or popularity.


## Hypotheses and validation

1. Tracks with higher audio 'danceability' and 'energy' have higher streams — validate using correlation and scatter plots.

2. Release timing affects streams (e.g., recency) — validate with time-series analysis.

3. Explicit tracks may have different streaming patterns — compare distributions.


## Project plan & roadmap

1. Data ingestion & cleaning (this repo)
2. EDA and feature engineering
3. Model prototyping (time-series/regression)
4. Dashboard development (Streamlit)
5. Deployment and monitoring


## Data visualization mapping

- Overview KPIs: total streams, average popularity, track count.
- Trends: streams over time, moving averages.
- Distribution: popularity, duration, acoustic features.
- Comparisons: top tracks, album-wise breakdown.


## Analysis techniques used

- Descriptive statistics
- Correlation analysis
- Visual EDA (histograms, boxplots, scatter)
- Time-series smoothing and forecasting (ARIMA/Prophet)
- Regression / tree-based models for prediction


## Limitations and alternative approaches

- Dataset may be incomplete or biased toward certain releases.
- External factors (marketing, playlisting) not captured.
- Alternatives: enrich with Spotify API metadata, social metrics, playlist placements.


## Ethical considerations

- Avoid overinterpreting correlations as causation.
- Respect artist intellectual property and privacy.
- Be transparent about model limitations and biases.


## Dashboard design & deployment (Streamlit)

- A sidebar for filters (year, album, explicit, popularity range).
- Main area: KPI tiles, interactive plots, top-N tables.
- Deploy with `streamlit run streamlit_app.py` or containerize with Docker.


## Challenges & solutions

- Missing values: impute or drop depending on importance.
- Large file sizes: sample or use chunked processing.


## Future improvements

- Integrate Spotify API for live updates.
- Add user authentication and personalized views.


## Technologies used

- Python, Pandas, NumPy, scikit-learn, Prophet/ARIMA, Matplotlib/Altair/Plotly, Streamlit.


## Main data analysis libraries

- pandas, numpy, matplotlib, seaborn, plotly, scikit-learn, statsmodels, prophet


## Credits

- Data provider: (your dataset)
- Project author: (your name)


## Conclusion & Acknowledgements

- This README pairs with the Jupyter notebook that contains hands-on analysis and code.
