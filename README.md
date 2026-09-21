# PRCP-1015 — Earthquake Damage Prediction

## 📌 Project Overview

Earthquakes can cause severe damage to buildings and infrastructure, resulting in significant economic losses and threats to human safety. The extent of building damage depends on several factors, including building structure, materials, age, location, height, foundation, and other construction characteristics.

This project applies **Machine Learning techniques** to analyze building-related data and predict the level of damage caused by an earthquake.

The project includes exploratory data analysis, data preprocessing, feature analysis, machine learning model development, model comparison, evaluation, and recommendations that may help seismologists and disaster-management professionals understand factors associated with significant building damage.

---

## 🎯 Problem Statement

The objective of this project is to predict the ordinal variable **`damage_grade`**, which represents the level of damage sustained by a building during an earthquake.

There are three damage grades:

| Damage Grade | Description                 |
| -----------: | --------------------------- |
|        **1** | Low damage                  |
|        **2** | Medium damage               |
|        **3** | Almost complete destruction |

### Project Tasks

**Task 1 — Data Analysis**

Prepare a complete data analysis report on the given earthquake building-damage dataset.

**Task 2 — Predictive Modeling**

Develop a predictive machine learning model to classify buildings according to their earthquake damage grade.

**Task 3 — Suggestions for Seismologists**

Analyze the results and provide data-driven suggestions that could help seismologists and disaster-management professionals understand building characteristics associated with severe earthquake damage.

---

## 🌍 Domain

**Disaster Management / Earthquake Damage Prediction / Machine Learning**

---

## 📊 Dataset Information

The dataset contains information about buildings located in regions affected by the **Gorkha earthquake**.

Each row represents a building, and the dataset contains **39 columns**:

* `building_id` — unique building identifier
* 38 building and geographic features

The features describe aspects such as:

* Geographic location
* Building age
* Number of floors
* Building area and height
* Foundation type
* Roof type
* Ground-floor type
* Construction materials
* Building position
* Ownership status
* Number of families
* Secondary building usage

Categorical variables have been obfuscated using lowercase characters.

---

## 🎯 Target Variable

The target variable is:

```text
damage_grade
```

It represents the severity of earthquake damage:

```text
1 → Low Damage
2 → Medium Damage
3 → Almost Complete Destruction
```

Since `damage_grade` is an **ordinal variable**, the ordering of the classes is meaningful.

---

## 🏗️ Important Features

### Geographic Features

* `geo_level_1_id`
* `geo_level_2_id`
* `geo_level_3_id`

These identify the geographic region of the building at different levels of specificity.

### Building Characteristics

* `count_floors_pre_eq`
* `age`
* `area_percentage`
* `height_percentage`
* `count_families`

### Construction Features

* `foundation_type`
* `roof_type`
* `ground_floor_type`
* `other_floor_type`
* `land_surface_condition`
* `position`
* `plan_configuration`

### Superstructure Features

The dataset includes indicators describing construction materials such as:

* Adobe/Mud
* Mud Mortar–Stone
* Stone
* Cement Mortar–Stone
* Mud Mortar–Brick
* Cement Mortar–Brick
* Timber
* Bamboo
* Non-engineered reinforced concrete
* Engineered reinforced concrete
* Other materials

### Ownership and Usage

* `legal_ownership_status`
* `has_secondary_use`
* `has_secondary_use_agriculture`
* `has_secondary_use_hotel`
* `has_secondary_use_rental`
* `has_secondary_use_institution`
* `has_secondary_use_school`
* `has_secondary_use_industry`
* `has_secondary_use_health_post`
* `has_secondary_use_gov_office`
* `has_secondary_use_use_police`
* `has_secondary_use_other`

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Missing Value & Duplicate Analysis
   ↓
Feature Analysis
   ↓
Categorical Feature Encoding
   ↓
Feature Scaling (where required)
   ↓
Train-Test Split
   ↓
Machine Learning Models
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Final Model Analysis
   ↓
Damage Prediction
   ↓
Recommendations
```

---

## 🧹 Data Preprocessing

The dataset is prepared for machine learning through appropriate preprocessing techniques.

The preprocessing stage includes:

* Loading the dataset
* Inspecting data dimensions
* Checking data types
* Checking missing values
* Checking duplicate records
* Identifying categorical and numerical features
* Analyzing the target distribution
* Encoding categorical variables
* Scaling numerical features where required
* Splitting the dataset into training and testing sets

---

## 📈 Exploratory Data Analysis

The EDA section investigates relationships between building characteristics and earthquake damage.

The analysis includes:

* Dataset overview
* Statistical summaries
* Damage-grade distribution
* Numerical feature distributions
* Categorical feature analysis
* Building age analysis
* Number of floors analysis
* Geographic feature analysis
* Construction-material analysis
* Correlation analysis
* Outlier analysis
* Feature relationships with `damage_grade`

Visualization techniques may include:

* Histograms
* Bar charts
* Box plots
* Count plots
* Correlation heatmaps

---

## 🤖 Machine Learning Models

Multiple classification algorithms are evaluated to predict earthquake damage grades.

Depending on the models implemented in the notebook, the comparison may include:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Gradient Boosting
* Other suitable classification algorithms

> **Note:** The final list of models should match the algorithms actually implemented in the Jupyter Notebook.

---

## 📊 Model Evaluation

The models are evaluated using appropriate classification metrics.

### Accuracy

Measures the percentage of correctly classified buildings.

### Precision

Measures how accurately the model predicts each damage category.

### Recall

Measures how effectively the model identifies buildings belonging to each actual damage category.

### F1-Score

Provides a balance between precision and recall.

### Confusion Matrix

The confusion matrix helps identify which damage grades are being correctly classified and which classes are being confused with one another.

### Classification Report

A classification report is used to summarize precision, recall, and F1-score for each damage category.

---

## 📋 Model Comparison Report

Multiple machine learning models are compared based on their performance.

Example format:

| Model               | Accuracy | Precision | Recall | F1-Score |
| ------------------- | -------: | --------: | -----: | -------: |
| Logistic Regression |        — |         — |      — |        — |
| Decision Tree       |        — |         — |      — |        — |
| Random Forest       |        — |         — |      — |        — |
| SVM                 |        — |         — |      — |        — |
| KNN                 |        — |         — |      — |        — |

The final model selection should be based on the **actual results obtained from the experiments in the notebook**, along with factors such as generalization, computational requirements, interpretability, and suitability for deployment.

---

## ⚠️ Challenges Faced

### 1. Large Number of Features

The dataset contains numerous geographic, structural, material, ownership, and usage-related variables.

**Technique used:** Exploratory data analysis and feature analysis are used to understand the contribution and distribution of different variables.

---

### 2. Categorical Variables

Several building characteristics are represented as categorical variables.

**Technique used:** Appropriate categorical encoding is applied before training machine learning models.

---

### 3. Geographic Features

The geographic-level features can contain many distinct values.

**Technique used:** These variables are analyzed carefully and encoded appropriately to avoid inefficient or inappropriate preprocessing.

---

### 4. Class Distribution

The number of buildings belonging to each damage grade may not be perfectly balanced.

**Technique used:** Class distribution is analyzed before model training, and suitable evaluation metrics are considered instead of relying only on accuracy.

---

### 5. Ordinal Target Variable

`damage_grade` contains ordered categories:

```text
1 < 2 < 3
```

This means the difference between low, medium, and severe damage has an inherent order.

**Technique used:** Classification models are evaluated while considering the ordinal nature of the target variable and class-level performance.

---

### 6. Model Overfitting

Complex models may learn patterns specific to the training dataset instead of generalizing to unseen buildings.

**Techniques used:**

* Train-test split
* Cross-validation where applicable
* Hyperparameter tuning
* Regularization
* Comparison of training and testing performance

---

## 🏛️ Suggestions for Seismologists and Disaster Management

The analysis can potentially assist professionals in identifying building characteristics associated with higher levels of earthquake damage.

Possible applications include:

* Identifying structural characteristics associated with severe damage
* Prioritizing vulnerable buildings for inspection
* Supporting earthquake preparedness planning
* Identifying areas requiring detailed structural assessment
* Supporting risk-mapping activities
* Improving building-safety assessment strategies
* Using historical building data to support disaster preparedness

The model should be considered a **decision-support and risk-analysis tool**, rather than a replacement for structural engineering assessments or official seismic-risk evaluations.

---

## 🛠️ Technologies Used

* **Python**
* **Jupyter Notebook**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**

> The final `requirements.txt` should contain the packages actually used in the notebook.

---

## 📁 Project Structure

```text
PRCP-1015-EquakeDamagePred/
│
├── PRCP-1015_Earthquake_Damage_Prediction.ipynb
├── README.md
├── requirements.txt
└── dataset/
    └── earthquake_damage.csv
```

The dataset can be excluded from the repository when appropriate, particularly if it is large or subject to separate distribution terms.

---

## ▶️ How to Run the Project

### Step 1 — Download the Repository

Download the repository from GitHub.

### Step 2 — Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3 — Start Jupyter Notebook

```bash
jupyter notebook
```

### Step 4 — Open the Notebook

```text
PRCP-1015_Earthquake_Damage_Prediction.ipynb
```

### Step 5 — Run the Notebook

Run the cells sequentially to reproduce:

```text
Data Analysis
      ↓
Preprocessing
      ↓
Feature Engineering
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Comparison
      ↓
Damage Grade Prediction
```

---

## 📓 Notebook Contents

All required tasks are completed in a **single Jupyter Notebook**, according to the project requirements.

The notebook contains:

1. Importing required libraries
2. Loading the dataset
3. Understanding the dataset
4. Data cleaning
5. Exploratory Data Analysis
6. Missing-value analysis
7. Duplicate analysis
8. Target-variable analysis
9. Feature analysis
10. Categorical feature encoding
11. Data preprocessing
12. Train-test splitting
13. Machine learning model development
14. Model training
15. Model evaluation
16. Confusion matrix analysis
17. Model comparison
18. Challenges faced
19. Recommendations for earthquake-risk analysis
20. Final conclusions

---

## 🚀 Future Improvements

Possible future improvements include:

* Using larger and more diverse earthquake datasets
* Applying advanced feature engineering
* Exploring ordinal classification techniques
* Performing extensive hyperparameter optimization
* Using ensemble learning approaches
* Applying explainable AI techniques
* Developing geographic risk visualizations
* Integrating GIS data
* Incorporating additional structural and seismic parameters
* Developing a building-risk assessment dashboard

---



## 👩‍💻 Author

**Aishwarya D**

B.Tech — Computer Science & Engineering
Specialization: Artificial Intelligence & Machine Learning

---

## 📌 Project Information

**Project ID:** PRCP-1015
**Project:** Earthquake Damage Prediction
**Domain:** Disaster Management / Machine Learning
**Task Type:** Multi-Class Classification
**Target Variable:** `damage_grade`
**Platform:** Jupyter Notebook
**Technology:** Python / Machine Learning
# Earthquake-damage-prediction
