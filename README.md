# COVID-19 Data Analysis & Forecasting

A data analysis and forecasting project built on the `covid_19_clean_complete.csv` dataset. The notebook explores confirmed, active, recovered, and death cases across countries, visualizes global trends, and uses Facebook's **Prophet** library to forecast future confirmed cases and deaths.

## 📌 Project Overview

This project walks through:

- **Data Cleaning** – loading the dataset, renaming columns (`Province/State` → `State`, `Country/Region` → `Country`), and inspecting data types.
- **Exploratory Data Analysis (EDA)** – aggregating confirmed, recovered, active, and death cases by date and by country, and identifying the top countries by recovered cases.
- **Country-wise Comparison** – comparing death trends across the US, India, and China using point plots.
- **Time-Series Forecasting** – using Prophet to forecast:
  - Confirmed cases for the next 60 days
  - Deaths for the next 15 days
- **Geospatial Visualization** – interactive choropleth maps (via Plotly) showing active cases, deaths, and recovered cases by country.

## 🛠️ Tech Stack

- **Python 3**
- **pandas**, **numpy** – data manipulation
- **matplotlib**, **seaborn** – static visualizations
- **plotly** – interactive choropleth maps
- **prophet** – time-series forecasting

## 📂 Dataset

The notebook expects a CSV file named `covid_19_clean_complete.csv` with columns including:

`Province/State`, `Country/Region`, `Date`, `Confirmed`, `Recovered`, `Active`, `Deaths`

> Update the file path in the notebook (`pd.read_csv(...)`) to point to wherever you place the dataset locally, e.g. `data/covid_19_clean_complete.csv`.

You can find similar COVID-19 datasets on [Kaggle](https://www.kaggle.com/datasets/imdevskp/corona-virus-report).

### 2. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn plotly prophet
```

### 3. Add the dataset
Place `covid_19_clean_complete.csv` in the project folder (or update the path in the notebook).

### 4. Run the notebook
```bash
jupyter notebook COVID1_19_PROJECT.ipynb
```

## 📊 Key Visualizations

- Global time-series trends of confirmed, active, recovered, and death cases
- Top 10 countries by recovered cases
- Death trend comparison: US vs. India vs. China
- Prophet forecast plots for confirmed cases (60-day) and deaths (15-day)
- Choropleth maps of active cases, deaths, and recovered cases by country

## 🔮 Forecasting Approach

The project uses **Prophet**, an open-source forecasting library developed by Facebook, well-suited for time-series data with trends and seasonality. Two separate models are trained:

1. One on aggregated global **confirmed cases** over time
2. One on aggregated global **deaths** over time

Each model generates a future dataframe and predicts values beyond the historical range of the dataset.

## 📝 Notes

- This project was built for learning/practice purposes around EDA and time-series forecasting.
- Forecasts are based on historical aggregated data and should not be used for real-world epidemiological decision-making.

## 🙋 Author

Feel free to connect or raise an issue if you have suggestions for improvement.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
