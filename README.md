# Urban Road Accident Risk Prediction

## Project Overview
This project predicts **high-risk urban road segments** using historical traffic accident data, weather conditions, road types, and temporal features. The goal is to identify **accident hotspots** and provide data-driven insights for **urban road safety planning**.

The project leverages **machine learning** (Random Forest, Decision Tree) and **clustering techniques (K-Means)** to analyze accident patterns. It demonstrates end-to-end workflow including **data preprocessing, exploratory data analysis (EDA), feature engineering, predictive modeling, and result visualization**.

---

## Folder Structure

---

## Key Features & Workflow

1. **Data Preprocessing**
   - Convert timestamp to datetime and extract features like `hour`, `day_of_week`, `is_weekend`.
   - Encode categorical variables (`weather`, `road_type`) for ML.
   - Save processed dataset for modeling.

2. **Exploratory Data Analysis (EDA)**
   - Analyze accident patterns by **hour**, **day of week**, **weather**, and **road type**.
   - Visualize accident distribution and identify temporal trends.
   - Perform **K-Means clustering** to detect accident hotspots geographically.

3. **Predictive Modeling**
   - Train **Random Forest** and **Decision Tree** classifiers to predict high-risk segments (`severity >= 3`).
   - Evaluate models using **accuracy, precision, recall, F1-score**, and **confusion matrices**.
   - Identify **top 10 feature importances** to understand factors influencing accident severity.

4. **Results**
   - Visual plots in `results/` folder:
     - Accidents by Hour
     - Accidents by Day of Week
     - Accident Hotspot Clustering
     - Confusion Matrix for Random Forest
     - Feature Importance (Random Forest)

---

## Dataset

- **Sample Dataset**: `data/accidents_sample.csv` (~50k rows)  
- **Columns**:  
  - `latitude`, `longitude` — GPS coordinates of accidents  
  - `weather` — Weather conditions at time of accident  
  - `road_type` — Type of road (Urban, Highway, Rural)  
  - `severity` — Accident severity (1=low, 4=high)  
  - `hour`, `day_of_week`, `is_weekend` — Derived temporal features  
- Full dataset can be obtained from [Kaggle US Accidents Dataset](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents).

> Note: The sample dataset is provided for reproducibility and GitHub size limitations.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yeshika11062006-ops/Urban-Accident-Risk-Prediction.git
cd URBAN-ACCIDENT-RISK-PREDICTION
pip install -r requirements.txt
