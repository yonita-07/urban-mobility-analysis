# Urban Mobility Delay Analysis

A complete end‑to‑end data science project with EDA, feature engineering and predictive modeling.

## Overview

This project analyzes ~77k train records from 20 major German cities and builds a **binary classification** model to predict whether a train will be delayed.

It includes:
- Data cleaning
- Exploratory data analysis (EDA)
- Visualisations
- Feature engineering
- Model training using Logistic Regression
- Hyperparameter tuning
- Evaluation
- Final insights

## Project Structure

```text
Urban_mobility_analysis/
├── data/
│   └── cleaned_train_delays_full.csv
├── notebooks/
│   ├── urban-mobility-analysis-code.ipynb      
│   └── report/
│       └── urban_mobility_analysis.ipynb      
└── README.md
```

## Data Description

- **Dates covered:** July–September 2024  
- **Stations:** 20 largest city main stations (Hbf) in Germany  
- **Columns include:**
  - `date`
  - `Hbf` (station)
  - `scheduled_time`
  - `expected_time`
  - `train_model`
  - `route`
  - `platform`
  - `real_time_due_to_delay`
  - `has_delay` (target variable: 1 = delayed, 0 = on time)

## Key Insights from Analysis

**1. On‑time vs delayed trains**
- ~22% of all trains experienced delays.

**2. Delay patterns**
- Delay peaks during morning and evening rush hours.
- Some stations consistently show higher delay frequencies.

**3. Daily trend**
- Delay rates fluctuate based on operational load and weekday patterns.

**4. Feature relationships**
- Station, route and train model influence delay probability.

## Machine Learning Model

- **Model used:** Logistic Regression  
- **Hyperparameter tuning:** `RandomizedSearchCV`

**Final Model Performance**

| Metric    | Score  |
|----------|--------|
| Accuracy | 84.89% |
| Precision| 83.82% |
| Recall   | 81.75% |
| F1 Score | 82.77% |

The model performs well despite natural class imbalance and remains interpretable.

## Visualizations Included

- Delay distribution histogram  
- Delay by station  
- Delay patterns by hour of the day  
- Delay trend over time  

All charts are included in the report notebook:  
`notebooks/report/urban_mobility_analysis.ipynb`

## Conclusion

- Train delays show clear **hourly** and **station‑based** patterns.
- A simple Logistic Regression model predicts delays with ~85% accuracy.
- Operational factors (station, load, train type) play a major role in delay likelihood and can be used to prioritize interventions.

## 🛠️ Technical Skills

- **Languages & Libraries:** Python 3.10, pandas, numpy, matplotlib, seaborn, scikit‑learn  
- **Machine Learning:** Logistic Regression, train/test split, class imbalance handling, hyperparameter tuning (RandomizedSearchCV)  
- **Data Work:** Data cleaning, feature engineering, time‑based analysis, EDA and visualization  
- **Tools:** Jupyter Notebook, Git/GitHub

## Future Work

- Integrate external factors (weather, events, maintenance logs)
- Experiment with gradient boosting models (XGBoost, LightGBM)
- Build an interactive Streamlit dashboard
- Add geospatial visualisation for route‑level delay mapping
```


 * [data](Urban_mobility_analysis/data)
   * [cleaned_train_delays_full.csv](Urban_mobility_analysis/data/cleaned_train_delays_full.csv)
 * [notebooks](Urban_mobility_analysis/notebooks)
   * [urban-mobility-analysis-code.ipynb](Urban_mobility_analysis/notebooks/urban-mobility-analysis-code.ipynb)
   * [report](Urban_Mobility_Analysis/notebooks/report)
     * [urban_mobility_analysis.ipynb](Urban_mobility_analysis/notebooks/report/urban_mobility_analysis.ipynb)
 * [README.md](Urban_mobility_analysis/README.md)


  
## Future Work
- Integrate external factors (weather, events, maintenance logs)
- Experiment with gradient boosting models(XGBoost, LightGBM)
- Build an interactive Streamlit dashboard
- Add geospatial visualisation for route-level delay mapping
