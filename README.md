# StartedFromTheData 
StartedFromTheData explores Drake’s complete Spotify discography using track-level metadata. The dataset includes 662 tracks across 36 features, covering identifiers, album and release details, audio features (danceability, energy, valence, tempo, etc.), track popularity, duration, and Spotify URLs. This foundation enables both descriptive analytics (trends, patterns, visualisations) and predictive modeling (popularity and streaming forecasts).


## Dataset content


| Column                  | Type     | Missing | Unique |
|--------------------------|----------|---------|--------|
| artist_name              | object   | 0       | 1      |
| artist_id                | object   | 0       | 1      |
| album_id                 | object   | 0       | 39     |
| album_type               | object   | 0       | 1      |
| album_release_date       | object   | 0       | 19     |
| album_release_year       | int64    | 0       | 12     |
| album_release_date_precision | object | 0      | 2      |
| danceability             | float64  | 0       | 345    |
| energy                   | float64  | 0       | 358    |
| key                      | int64    | 0       | 12     |
| loudness                 | float64  | 0       | 511    |
| mode                     | int64    | 0       | 2      |
| speechiness              | float64  | 0       | 386    |
| acousticness             | float64  | 0       | 446    |
| instrumentalness         | float64  | 0       | 245    |
| liveness                 | float64  | 0       | 278    |
| valence                  | float64  | 0       | 385    |
| tempo                    | float64  | 0       | 539    |
| track_id                 | object   | 0       | 662    |
| analysis_url             | object   | 0       | 662    |
| time_signature           | int64    | 0       | 4      |
| disc_number              | int64    | 0       | 2      |
| duration_ms              | int64    | 0       | 355    |
| explicit                 | bool     | 0       | 2      |
| track_href               | object   | 0       | 662    |
| is_local                 | bool     | 0       | 1      |
| track_name               | object   | 0       | 247    |
| track_preview_url        | float64  | 662     | 1      |
| track_number             | int64    | 0       | 22     |
| type                     | object   | 0       | 1      |
| track_uri                | object   | 0       | 662    |
| external_urls.spotify    | object   | 0       | 662    |
| album_name               | object   | 0       | 18     |
| key_name                 | object   | 0       | 12     |
| mode_name                | object   | 0       | 2      |
| key_mode                 | object   | 0       | 24     |


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
- Deploy with `streamlit run streamlit_app.py` 


## Challenges & solutions

- Missing values: impute or drop depending on importance.
- Large file sizes: sample or use chunked processing.


## Future improvements

- Integrate Spotify API for live updates.
- Add user authentication and personalized views.


### Technologies Used

| Technology      | Purpose                                                                 |
|-----------------|-------------------------------------------------------------------------|
| Python          | Core programming language for data analysis, modeling, and dashboards.  |
| Pandas          | Data manipulation and cleaning (DataFrames, filtering, aggregation).    |
| NumPy           | Numerical computing and efficient array operations.                     |
| scikit-learn    | Machine learning algorithms, preprocessing, and evaluation.             |
| Prophet / ARIMA | Time-series forecasting and trend analysis.                             |
| Matplotlib      | Foundational plotting library for static visualizations.                |
| Altair          | Declarative statistical visualizations.                                 |
| Plotly          | Interactive charts and dashboards (used in Streamlit).                  |
| Streamlit       | Web app framework for interactive data dashboards.                      |

---

### Main Data Analysis Libraries

| Library        | Purpose                                                                 |
|----------------|-------------------------------------------------------------------------|
| pandas         | Data wrangling, cleaning, and tabular data analysis.                    |
| numpy          | Mathematical operations, linear algebra, and array handling.            |
| matplotlib     | Base plotting library for static charts and customization.              |
| seaborn        | Statistical visualization built on top of matplotlib.                   |
| plotly         | Interactive and dynamic charts for EDA and dashboards.                  |
| scikit-learn   | ML models, preprocessing, feature engineering, and validation.          |
| statsmodels    | Advanced statistical modeling (regression, ARIMA, hypothesis testing).  |
| prophet        | High-level library for time-series forecasting and trend modeling.      |


## Credits

- Data provider: [Kaggle](https://www.kaggle.com/datasets/arthurboari/drake-spotify-data?resource=download)
- Project author: Tamika Mqhum 


## Conclusion & Acknowledgements

- This README pairs with the Jupyter notebook that contains hands-on analysis and code.
