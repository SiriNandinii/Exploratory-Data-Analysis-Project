<div align="center">

# 🌍 Earthquake Data Analysis & Machine Learning

**An end-to-end Machine Learning workflow for earthquake magnitude prediction**

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)

[![License](https://img.shields.io/badge/License-Educational-blue?style=flat-square)](#-license)
[![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)](#)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square)](#)
[![Made with Love](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red?style=flat-square)](#)
![GitHub last commit](https://img.shields.io/badge/Maintained-Yes-informational?style=flat-square)

</div>

---

## 📖 Project Overview

This project demonstrates an **end-to-end Machine Learning workflow** applied to an earthquake dataset — from raw data to trained, evaluated, and visualized models.

<details>
<summary><strong>🔍 Click to expand: what the notebook covers</strong></summary>

- ✅ Data preprocessing
- ✅ Feature engineering
- ✅ Dataset export
- ✅ Train-test split
- ✅ Multiple Machine Learning models
- ✅ Model evaluation
- ✅ Data visualization
- ✅ Prediction on unseen data
- ✅ Feature importance analysis

</details>

**Goal:** Predict earthquake magnitude using geological parameters, and compare the effectiveness of different ML algorithms across both regression and classification tasks.

---

## 📂 Dataset

| Feature | Description |
|:--|:--|
| 🗓️ `Date` | Date of occurrence |
| ⏰ `Time` | Time (UTC) |
| 🧭 `Latitude` | Geographic latitude |
| 🧭 `Longitude` | Geographic longitude |
| 🕳️ `Depth` | Earthquake depth (km) |
| 📏 `Magnitude` | Earthquake magnitude |
| 🏷️ `Magnitude Type` | Scale used to measure magnitude |

> Columns are renamed during preprocessing for improved readability and consistency.

---

## 🛠️ Tech Stack

<div align="center">

| Category | Tools |
|:--|:--|
| **Language** | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **Environment** | ![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) |
| **Data Handling** | ![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat-square&logo=numpy&logoColor=white) |
| **Visualization** | ![Matplotlib](https://img.shields.io/badge/-Matplotlib-11557C?style=flat-square) ![Seaborn](https://img.shields.io/badge/-Seaborn-4C72B0?style=flat-square) |
| **Machine Learning** | ![Scikit-Learn](https://img.shields.io/badge/-Scikit--Learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white) |

</div>

---

## 📊 Project Workflow

```mermaid
flowchart LR
    A[📥 Data Import] --> B[🧹 Preprocessing]
    B --> C[✂️ Train/Test Split]
    C --> D[🤖 Model Training]
    D --> E[📈 Evaluation]
    E --> F[🎨 Visualization]
    F --> G[🔮 Prediction on Unseen Data]
```

### 1️⃣ Data Import
- Load earthquake dataset
- Inspect structure and data types

### 2️⃣ Data Preprocessing
- Rename columns for clarity
- Check missing values
- Verify datatypes
- Export processed dataset → `Earthquake_data_processed.xlsx`

### 3️⃣ Dataset Splitting
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

---

## 🤖 Machine Learning Models

<details open>
<summary><strong>1. 📈 Multiple Linear Regression</strong></summary>

Used for continuous magnitude prediction.

- Train model → Predict on test data → Predict on new data → Evaluate

**Metrics:** R² Score · MSE · RMSE
**Visualization:** Actual vs Predicted Scatter Plot

</details>

<details>
<summary><strong>2. 🧮 Support Vector Regression (SVR)</strong></summary>

Applies Support Vector Machines to a regression setting.

- Train model → Predict on test set → Predict unseen samples → Compare

**Metrics:** MSE · R² Score
**Visualization:** Regression Plot

</details>

<details>
<summary><strong>3. 🏷️ Naive Bayes Classification</strong></summary>

Used to predict **Magnitude Type** (categorical) rather than numerical magnitude.

- Train classifier → Predict magnitude type → Calculate accuracy → Visualize

**Metric:** Classification Accuracy

</details>

<details>
<summary><strong>4. 🌳 Random Forest Regression</strong></summary>

Combines multiple decision trees for improved prediction accuracy.

- Train model → Predict test set → Evaluate → Visualize

**Metrics:** MSE · R² Score
**Extras:** Feature Importance · Residual Plot · Scatter Plot

</details>

---

## 📈 Visualizations

| Type | Purpose |
|:--|:--|
| 🔵 Scatter Plot | Compare predicted vs actual values |
| 📉 Regression Plot | Visualize model fit |
| 🎯 Actual vs Predicted | Assess prediction quality |
| ⭐ Feature Importance Graph | Identify influential features |
| 📊 Residual Plot | Analyze error distribution |

---

## 📁 Project Structure

```
Earthquake-ML/
│
├── EDA.ipynb                          # Main analysis & modeling notebook
├── Earthquake_data_processed.xlsx     # Cleaned/processed dataset
├── dataset.csv                        # Raw dataset
└── README.md                          # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python)

### 1. Clone the repository
```bash
git clone https://github.com/SiriNandinii/Earthquake-ML.git
cd Earthquake-ML
```

### 2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Launch the notebook
```bash
jupyter notebook
```

### 4. Open and run
```
EDA.ipynb  →  Run All Cells ▶️
```

---

## 📊 Model Evaluation Summary

| Model | Type | Key Metrics |
|:--|:--|:--|
| Multiple Linear Regression | Regression | R², MSE, RMSE |
| Support Vector Regression | Regression | MSE, R² |
| Naive Bayes | Classification | Accuracy |
| Random Forest Regression | Regression | MSE, R², Feature Importance |

---

## 🎯 Learning Outcomes

- 🧹 Data preprocessing & feature engineering
- 📉 Regression techniques
- 🏷️ Classification techniques
- ⚖️ Model comparison & performance evaluation
- 🎨 Visualization of predictions
- ⭐ Feature importance analysis

---

## 🔮 Future Improvements

- [ ] Hyperparameter tuning
- [ ] Cross-validation
- [ ] Gradient Boosting
- [ ] XGBoost
- [ ] LightGBM
- [ ] CatBoost
- [ ] Deep Learning models
- [ ] Time-series forecasting
- [ ] Earthquake risk prediction dashboard
- [ ] Deployment using Flask or Streamlit

---

## ⭐ Key Highlights

<div align="center">

| ✅ | Highlight |
|:--:|:--|
| 🧭 | Clean and structured workflow |
| 🤖 | Multiple Machine Learning algorithms |
| 🔀 | Regression + Classification combined |
| 📊 | Comprehensive evaluation metrics |
| 🎨 | Visualization-rich notebook |
| 🌱 | Beginner-friendly implementation |

</div>

---

## 👩‍💻 Author

<div align="center">

**Siri Nandini Alanka**

*AI & Machine Learning Student | Full Stack Developer | Machine Learning Enthusiast*

[![GitHub](https://img.shields.io/badge/GitHub-SiriNandinii-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SiriNandinii)

</div>

---

## 📜 License

![License](https://img.shields.io/badge/License-Educational%20Use-blue?style=flat-square)

This project is intended for **educational and learning purposes**.

---

<div align="center">

### ⭐ If you found this project helpful, consider giving it a star!

</div>
