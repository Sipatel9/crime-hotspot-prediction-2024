# Crime Hotspot Prediction Using Python & Machine Learning (2024 Dataset) 📊

Python-based crime hotspot analysis and prediction system using advanced data science and machine learning techniques on the 2024 London crime dataset.

## 📋 Overview

This project implements comprehensive crime analysis and predictive modeling to:
- Analyze crime distribution across time, crime types, and geographic regions
- Identify crime hotspots using statistical thresholds
- Predict future crime locations with ML models
- Provide actionable insights for law enforcement and community safety

## 🎯 Features

✅ Comprehensive crime data analysis  
✅ Geographic hotspot identification  
✅ Predictive modeling with multiple algorithms  
✅ Temporal trend analysis  
✅ Statistical insights and patterns  
✅ Interactive visualizations  
✅ Ethical considerations framework  

## 📊 Dataset

- **Source**: London Crimes 2024 Expanded Dataset
- **Coverage**: Multiple London boroughs and LSOAs
- **Records**: Thousands of crime incidents
- **Features**: Crime type, location, date, outcome, coordinates

## 🏗️ Methodology

### 1. Data Cleaning
- Removed missing or invalid entries
- Standardized date formats
- Filled missing outcome categories
- Ensured required fields present

### 2. Feature Aggregation
Data grouped by:
- LSOA (Lower Super Output Area)
- Month and Year
- Crime Type

Generated:
- Total crime count per LSOA-month
- Crime-type pivot tables
- Monthly ordering for temporal analysis

### 3. Hotspot Definition
**Hotspots = LSOA-months in the top 10% of crime counts**

### 4. Lagged Features
Created previous-month features to:
- Prevent data leakage
- Simulate real prediction scenarios
- Capture temporal dependencies

### 5. Modeling
Models evaluated:
- **Logistic Regression** - Baseline linear model
- **Random Forest Classifier** - Non-linear patterns

Train/test split based on **time**, not random shuffle.

## 📈 Results Summary

### Logistic Regression
- **Accuracy**: 0.916
- **Precision**: 0.577
- **Recall**: 0.908
- **F1-Score**: 0.706

### Random Forest (Best Performer)
- **Accuracy**: 0.939
- **Precision**: 0.681
- **Recall**: 0.850
- **F1-Score**: 0.756

Random Forest performed best due to its ability to capture non-linear relationships in crime patterns.

## 📊 Visual Outputs

All analysis and model results are visualized in the `figures/` folder:

- **Crime Type Distribution** - Bar chart of top 10 crime types
- **Monthly Crime Trend** - Time series of crime over months
- **Spatial Distribution** - Scatter plot of crime incidents
- **Top LSOAs** - Regions with highest crime counts
- **Confusion Matrices** - Logistic Regression and Random Forest
- **Feature Importance** - Top predictive features from Random Forest
- **Model Comparison** - Performance metrics table

## 🧬 Feature Engineering

### Key Features
| Feature | Description |
|---------|-------------|
| **lagged_crime_count** | Previous month total crimes |
| **crime_type_lags** | Previous month crime-specific counts |
| **lagged_is_hotspot** | Was it a hotspot last month? |
| **trend_features** | Month-over-month changes |
| **seasonal_features** | Monthly seasonality patterns |

## 🏗️ System Architecture

```
Raw Crime Data
    ↓
Data Cleaning & Validation
    ↓
Feature Aggregation (LSOA-Month)
    ↓
Hotspot Definition (Top 10%)
    ↓
Lagged Feature Creation
    ↓
Train/Test Split (Time-based)
    ↓
Model Training
    ├── Logistic Regression
    └── Random Forest
    ↓
Evaluation & Metrics
    ↓
Visualization & Insights
```

## 📁 Repository Structure

```
├── data/
│   └── London_Crimes_2024_Expanded.csv
├── notebooks/
│   ├── data_cleaning.ipynb
│   ├── feature_engineering.ipynb
│   ├── modeling.ipynb
│   └── evaluation.ipynb
├── figures/
│   ├── top_crime_types.png
│   ├── monthly_trend.png
│   ├── spatial_distribution.png
│   ├── top_lsoas.png
│   ├── confusion_matrix_logreg.png
│   ├── confusion_matrix_rf.png
│   └── feature_importance_rf.png
├── src/
│   ├── data_processor.py
│   ├── feature_engineer.py
│   ├── models.py
│   └── evaluation.py
└── README.md
```

## 🚀 Getting Started

### Prerequisites
```bash
python >= 3.8
pandas, numpy, scikit-learn
matplotlib, seaborn, folium
geopandas, shapely
jupyter
```

### Installation
```bash
git clone https://github.com/Sipatel9/crime-hotspot-prediction-2024.git
cd crime-hotspot-prediction-2024
pip install -r requirements.txt
```

### Running the Analysis
```bash
# Start Jupyter
jupyter notebook

# Open and run notebooks in this order:
# 1. data_cleaning.ipynb
# 2. feature_engineering.ipynb
# 3. modeling.ipynb
# 4. evaluation.ipynb
```

## 💡 Key Insights

- **Geographic Clustering** - Clear concentration of crime in specific LSOAs
- **Temporal Patterns** - Seasonal and day-of-week variations in crime
- **Crime Type Variation** - Different crimes concentrate in different areas
- **Predictability** - Hotspots show temporal persistence (Random Forest: 85% recall)

## 🎓 Technologies

- **Pandas/NumPy** - Data manipulation and numerical computing
- **Scikit-learn** - Machine learning and evaluation
- **Matplotlib/Seaborn** - Static visualizations
- **Folium** - Interactive geographic maps
- **GeoPandas** - Geospatial analysis

## ⚖️ Ethical Considerations

- **Predictive Policing Bias** - Models may reinforce historical bias in policing
- **Data Limitations** - Crime data reflects police activity, not true crime rate
- **Responsible AI** - Models should support, not replace, human decision-making
- **Fairness** - Ensure equitable resource allocation across communities
- **Transparency** - Stakeholders must understand model limitations

## 📘 Full Report

The complete academic report is included in the `report/` folder, covering:
- Research questions and stakeholder analysis
- Data cleaning and preprocessing
- Feature engineering methodology
- Model selection and training
- Comprehensive evaluation metrics
- Ethical considerations and limitations

[Full Report Document](report/DataScience_Assignment_2.docx)

## 🔗 Resources

- 📊 [Google Colab Notebook](https://colab.research.google.com/drive/1BK3TsgQQ5m9_oOCCO9z0o3RfrotDEy5I?usp=sharing)
- 📚 [Crime Data Documentation](https://data.london.gov.uk/)
- 🗺️ [LSOA Geographic Data](https://geoportal.statistics.gov.uk/)

## 🤝 Contributing

Contributions welcome! Help us:
- Improve prediction accuracy
- Add new visualization types
- Expand to other datasets/regions
- Optimize performance
- Enhance ethical framework

## 📝 License

MIT License - Open for research and educational use

## 👩‍💻 Author

**Samira Patel**  
BSc (Hons) Computer Science  
University of Central Lancashire (UCLan)

## 📞 Contact

Questions about the analysis? [Reach out](https://github.com/Sipatel9)

---

**⭐ If you found this analysis valuable, please star it!**
