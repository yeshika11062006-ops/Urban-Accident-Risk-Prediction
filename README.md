
# Urban Accident Risk Prediction

A Machine Learning project that analyzes traffic accident data and predicts **high-risk accident scenarios** using real-world accident datasets.

The goal of this project is to identify patterns in accident occurrences and build predictive models that can help understand factors contributing to accident severity.

---

# Project Motivation

Road accidents are one of the leading causes of injuries and fatalities worldwide. Understanding when and why accidents happen can help improve traffic safety and decision-making.

By analyzing accident data using machine learning techniques, this project aims to:

* Discover patterns in accident occurrences
* Analyze how factors like **time, weather, and environment** affect accidents
* Predict **high-risk accident situations**
* Visualize accident trends for better understanding

---

# Dataset

This project uses the **US Accidents dataset**, which contains large-scale real-world accident records collected across multiple states.

Dataset features include:

* Accident severity
* Time and date of accident
* Weather conditions
* Temperature
* Humidity
* Visibility
* Wind speed
* Sunrise / sunset information

The original dataset is large (~3GB), so a subset of the data is used for training and analysis.

Dataset source:
Kaggle

---

# Project Structure

```
Urban-Accident-Risk-Prediction
│
├── data
│   ├── US_Accidents_March23.csv
│   └── accidents_processed.csv
│
├── notebook
│   ├── 1_data_preprocessing.ipynb
│   ├── 2_eda_visualization.ipynb
│   └── 3_predictive_modeling.ipynb
│
├── results
│   ├── accidents_by_hour.png
│   ├── accidents_by_day.png
│   ├── accidents_hour_trend.png
│   ├── weather_accidents.png
│   ├── correlation_heatmap.png
│   ├── confusion_rf.png
│   └── feature_importance_rf.png
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# Data Preprocessing

The preprocessing stage prepares the raw dataset for machine learning.

Steps performed:

1. Loading accident dataset
2. Selecting relevant features
3. Converting time features
4. Handling missing values
5. Encoding categorical variables
6. Creating additional time-based features
7. Saving the cleaned dataset

New features created:

* `hour` — hour of the accident
* `day_of_week` — day of the week
* `is_weekend` — weekend indicator

The processed dataset is saved as:

```
accidents_processed.csv
```

---

# Exploratory Data Analysis (EDA)

EDA helps understand patterns and trends in the accident dataset.

Visualizations generated include:

### Accidents by Hour

Shows which hours of the day have the highest accident frequency.

### Accidents by Day of Week

Analyzes which days experience more accidents.

### Accident Trend by Hour

Displays accident patterns throughout the day.

### Weather Conditions During Accidents

Identifies which weather conditions contribute most to accidents.

### Correlation Heatmap

Shows relationships between numerical features.

These visualizations are saved in the `results` folder.

---

# Machine Learning Models

Two machine learning models were implemented to predict **high-risk accidents**.

### 1. Random Forest Classifier

Random Forest is an ensemble learning algorithm that builds multiple decision trees and combines their predictions.

Advantages:

* Handles complex relationships
* Works well with tabular data
* Reduces overfitting

### 2. Decision Tree Classifier

Decision Trees split the dataset based on feature values to classify accident risk.

Advantages:

* Easy to interpret
* Simple and fast

---

# High-Risk Accident Definition

A **high-risk accident** is defined as:

```
Severity >= 3
```

This converts the severity prediction problem into a **binary classification task**:

* 0 → Low Risk Accident
* 1 → High Risk Accident

---

# Model Evaluation

Models are evaluated using:

* Precision
* Recall
* F1 Score
* Confusion Matrix

# Feature Importance

Random Forest also provides feature importance scores, showing which variables contribute most to predictions.

Typical important features include:

* Visibility
* Weather conditions
* Temperature
* Time of day

These insights help understand **key accident risk factors**.

---

# Technologies Used

Programming Language

* Python

Libraries

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn

Development Environment

* Visual Studio Code
* Jupyter Notebook

---

# Installation

Clone the repository:

```
git clone https://github.com/yourusername/urban-accident-risk-prediction.git
```

Move into the project folder:

```
cd urban-accident-risk-prediction
```

Install dependencies:

```
pip install -r requirements.txt
```

---

# Running the Project

Step 1 – Run preprocessing notebook

```
1_data_preprocessing.ipynb
```

Step 2 – Run exploratory data analysis

```
2_eda_visualization.ipynb
```

Step 3 – Train machine learning models

```
3_predictive_modeling.ipynb
```

---

# Results

The project produces:

* Accident trend visualizations
* Weather impact analysis
* Correlation analysis
* Random Forest predictions
* Feature importance graphs
* Confusion matrices

All outputs are saved in the `results` directory.

---

# Future Improvements

Possible extensions for this project:

* Deep learning models
* Geographic accident heatmaps
* Real-time accident prediction
* Integration with traffic data
* Accident risk prediction dashboard

---

# Applications

This system could help:

* Traffic safety agencies
* Urban planners
* Smart city systems
* Emergency response planning

Predicting high-risk accident situations can contribute to **safer road infrastructure and better traffic management**.

---


