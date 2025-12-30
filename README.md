# CropYieldPrediction

# 🌾 Crop Yield Prediction Using Environmental Data

**Author:** Jake Walkup  
**Tools:** Python, Pandas, NumPy, Scikit-learn, Plotly, Matplotlib  
**Project Type:** Exploratory Data Analysis, Statistical Testing, Regression Modeling

---

## 📌 Project Overview

This project explores how environmental and farm management variables influence agricultural crop yield. Using a dataset of 3,000 simulated farms, I investigate which factors most strongly affect yield, perform hypothesis testing using a permutation test, and build a regression model to predict crop yield.

**Goal:** Identify the most important predictors of crop yield and evaluate whether farm size alone can accurately predict production outcomes.

---

## 📊 Dataset

Source: Kaggle (simulated data)

| Feature | Description |
|--------|-------------|
| rainfall_mm | Average rainfall during the growing season (500–2000 mm) |
| soil_quality_index | Soil quality score (1–10) |
| farm_size_hectares | Farm size (10–1000 hectares) |
| sunlight_hours | Average daily sunlight (4–12 hours) |
| fertilizer_kg | Fertilizer applied per hectare (100–3000 kg) |
| crop_yield | **Target variable:** crop yield in tons per hectare |

---

## 🔍 Exploratory Data Analysis

- Univariate distributions showed most features were evenly distributed.
- Bivariate analysis revealed that **farm size had the strongest relationship with crop yield**.
- Crop yield displayed a multimodal distribution, indicating possible subgroup behavior.

---

## 🧪 Hypothesis Testing

**Question:** Does farm size significantly affect crop yield?

- **Null Hypothesis (H₀):** Farm size has no effect.  
- **Alternative Hypothesis (H₁):** Farm size significantly affects yield.

A **permutation test with 10,000 shuffles** was performed.

**Results:**
- Observed correlation: **0.989**  
- p-value: **< 0.001**

**Conclusion:** Reject H₀ — farm size is significantly associated with crop yield.

---

## 🤖 Model – Linear Regression

| Metric | Value |
|-------|-------|
| R² | 0.978 |
| RMSE | 21.46 |
| Intercept | 78.5 |
| Coefficient (farm size) | 0.50 |

**Interpretation:**  
Each additional hectare is associated with an average increase of approximately **0.5 tons per hectare** in predicted crop yield.

---

## ⚠️ Limitations

- Dataset is simulated and unrealistically clean.  
- Real-world agricultural data would include missing values, noise, and confounding variables.  
- Interaction effects between variables are not modeled.

---

## 🚀 Future Improvements

- Use real-world datasets.  
- Build multivariate and non-linear models.  
- Analyze feature interactions.

---

## 🛠 How to Run

```bash
pip install pandas numpy scikit-learn plotly matplotlib
python crop_yield_analysis.py
