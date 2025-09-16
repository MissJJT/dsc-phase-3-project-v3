# 💧 Predicting the Functionality of Water Pumps in Tanzania

This repository contains a Jupyter notebook that details a machine learning project aimed at predicting the functional status of water pumps in Tanzania. The project was created as part of a competition on the Data Driven platform.

## 📌 Project Overview

Access to clean water remains a significant challenge in Tanzania. While many water points have been established, a substantial number have pumps that are either non-functional or in need of repair. This project aims to build a machine learning model that predicts the functionality status of water pumps based on various technical, geographic, and socio-economic features.

### 🎯 Objective

To classify water pumps into one of three categories:
- **Functional**
- **Functional but needs repair**
- **Non-functional**

This model can be used by the Tanzanian Ministry of Water and various NGOs to streamline their maintenance efforts and strategically allocate resources.This classification will help prioritize maintenance and resource allocation for water infrastructure.

---

## 📊 Dataset Description

The dataset is sourced from [DrivenData's "Pump It Up" competition](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/). It contains over 59,000 records with detailed attributes about each water point, including:

- **Geographic Info**: region, district, GPS coordinates
- **Technical Specs**: extraction type, construction year, installer
- **Socio-Economic Factors**: funder, management type, payment method
- **Water Quality & Quantity**: water source, quality group, quantity group

---

## 🧹 Data Preprocessing

Key steps include:
- Handling missing values
- Droping columns
- Feature Engineering - Age of Pump
- Converting date formats and extracting year
- Encoding categorical variables
- Scaling numerical features
- Addressing class imbalance using **SMOTE**

---

## 🧠 Modeling Approach

Several classification models were explored:
- Logistic Regression
- Random Forest
- XGBoost

Model tuning was performed using:
- RandomizedSearchCV

Evaluation metrics include:
- Accuracy
- Confusion Matrix
- Classification Report

---

## 📈 Results & Insights

- The dataset is highly imbalanced, with the majority labeled as **Functional**
- Geographic and management features showed strong predictive power
- Ensemble models like **Random Forest** and **XGBoost** performed best in terms of accuracy and generalization

The final, tuned XGBoost model achieved a high level of accuracy in predicting the status of the water pumps. While the model performed exceptionally well on the "functional" and "non-functional" classes, the confusion matrix revealed that it struggled to accurately identify the "functional but needs repair" class.

---
## 📌Conclusion and Reccommendations

The project successfully delivered a robust, optimized XGBoost model for predicting water pump functionality. This model is recommended for practical deployment.

However, to further enhance the model's predictive power, especially for the "functional needs repair" class, future data collection should focus on gathering more detailed information, such as:

The last service date of the well.

The types of repairs that were performed.

A specific list of parts that were replaced or repaired.

This richer data would provide the model with better signals to distinguish between a well that is working and one that is on the verge of failure.



## 📁 Repository Structure

```bash
.
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── status.csv
├── student.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Launch Jupyter Notebook and open `student.ipynb`
4. Run cells sequentially to preprocess data, train models, and evaluate results

---

## 🤝 Acknowledgments

- [DrivenData](https://www.drivendata.org/) for the dataset and competition
- Tanzania's water authorities and NGOs for their ongoing efforts in improving water access

---

