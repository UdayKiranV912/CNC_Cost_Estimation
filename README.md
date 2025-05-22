# CNC Cost Estimation using Machine Learning

This project demonstrates how machine learning can be applied to estimate the manufacturing cost of CNC-machined parts using features like material type, physical dimensions, and machining cycle time.

The project walks through data generation, cleaning, feature engineering, exploratory visualization, model training (Random Forest), and evaluation.

---

## 📁 Project Structure

```
CNC_Cost_Estimation/
├── CNC_Cost_Estimation.ipynb   # Main Jupyter notebook
├── README.md                   # Project overview and usage instructions
```

---

## 🔍 Project Overview

### Objective:
To build a predictive model that can estimate the quoted manufacturing cost of a CNC-machined part based on design and process features.

### Key Features Used:
- **Material type** (Aluminum, Steel, etc.)
- **Part dimensions** (Length, Width, Height)
- **Volume and Surface Area**
- **Cycle time** (estimated machining time)
- **Derived features** like:
  - Cost per mm³
  - Surface area to volume ratio

---

## 📊 Workflow Summary

### 1. Data Generation
- A synthetic dataset is created with randomized part dimensions and material types.
- Cost is calculated based on volume, material cost factor, and cycle time.

### 2. Data Cleaning & Exploration
- Checked for nulls and duplicates (none present due to synthetic generation).
- Descriptive statistics and visualizations are used to understand data patterns.

### 3. Feature Engineering
New features created to better capture machining cost dynamics:
- Cost per unit volume
- Surface area
- Surface-to-volume ratio

### 4. Visualization
Includes:
- Distribution of quoted cost
- Cycle time per material
- Cost vs volume scatter plots
- Correlation heatmap

### 5. Model Training
- Model: Random Forest Regressor
- Data split into training and test sets (80/20)
- Evaluation metrics used:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score
- Visual comparison of predicted vs actual cost
- Feature importance ranking

---

## 📈 Sample Results

Performance on test set (may vary due to random generation):
- **MAE** ≈ 135
- **RMSE** ≈ 172
- **R² Score** ≈ 0.91

---

## ✅ Insights & Takeaways

- Volume and cycle time were the most important predictors of cost.
- Surface area contributed to explaining machining complexity.
- Material type mattered but had a smaller impact relative to geometric/process features.

---

## 🔧 Possible Improvements

- Replace synthetic data with real-world machining cost data.
- Include advanced machining parameters (e.g., tool paths, speed/feed rates).
- Add part complexity metrics derived from CAD data.
- Try other models (XGBoost, Gradient Boosting, Neural Networks) for comparison.

---

## 📌 Requirements

You can run this project in Jupyter with the following Python packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 👨‍💻 Author

**Uday Kiran V**  
Feel free to reach out or contribute with suggestions and improvements.
