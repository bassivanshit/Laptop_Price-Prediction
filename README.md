
# 💻 Laptop Price Prediction Engine

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/Data%20Visualization-Seaborn%20%2F%20Matplotlib-11557C?style=for-the-badge&logo=pandas&logoColor=white" alt="Visualization">
  <img src="https://img.shields.io/badge/Data%20Science-Feature%20Engineering-blueviolet?style=for-the-badge" alt="Feature Engineering">
</p>

> **🎯 Project Core:** Transforming raw, messy e-commerce retail technical specifications into an accurate, data-driven pricing strategy engine using predictive machine learning pipelines.

---

## ⚡ Executive Recruiter Dashboard

> **🚀 Quick Take:** This repository bypasses generic model-fitting to focus heavily on advanced **text mining and regex-driven feature engineering** on real-world retail data. It builds an optimized regression pipeline that maps complex hardware specs directly to market value.

### 📊 Project Health & Metrics At A Glance
<table>
  <tr>
    <td><b>📈 Top Model Accuracy</b></td>
    <td>██████████████▒▒ 88% R² Variance Score</td>
    <td><b>🧹 Data Quality</b></td>
    <td>🟢 High (Cleaned & Parsed via Regex)</td>
  </tr>
  <tr>
    <td><b>⚙️ Pipeline State</b></td>
    <td>🟢 Production-Ready / Modular Architecture</td>
    <td><b>💡 Business Value</b></td>
    <td>🔥 High (Dynamic Pricing Strategy Intelligence)</td>
  </tr>
</table>

---

## 🧭 Interactive Project Pipeline & Deep Dive
*Click on any engineering phase below to instantly expand the deep dive and see exactly how the technical workflow was structured inside the notebook.*

<details>
<summary><b>🧹 Phase 1: Advanced Data Cleaning & Text Mining</b></summary>
<br>

*   **Noise Reduction:** Stripped static text flags (`GB`, `kg`) from structural numeric variables to transform them into raw statistical continuous datatypes.
*   **Handling Nulls & Anomalies:** Verified dataset integrity by parsing complex structural strings down to uniform baselines, eliminating analytical noise.
</details>

<details>
<summary><b>⚙️ Phase 2: Strategic Feature Engineering (The Code's Core)</b></summary>
<br>

Real-world commercial data doesn't come in neat numbers. The raw dataset contained unstructured records like: `"HP 15-bs011nv (i3-6006U/4GB/128GB/FHD/W10)"`

*   **Display Resolution Extraction:** Used string filtering and regex patterns to isolate specific high-value hardware features: **Touchscreen Capability (0/1)** and **IPS Panel Integration (0/1)**.
*   **Hardware Architecture Tiering:** 
    *   Mapped high-cardinality Central Processing Units (CPUs) into 5 highly predictive, low-cardinality groups (*Intel Core i7, Intel Core i5, Intel Core i3, AMD Processors, and Other/Budget variants*).
    *   Segmented Graphic Processing Units (GPUs) by brand equity to eliminate model bias.
</details>

<details>
<summary><b>📐 Phase 3: Mathematical Normalization & EDA</b></summary>
<br>

*   **The Discovery:** Initial testing showed a heavily right-skewed pricing distribution ($Price$ had a long tail due to premium gaming systems). Parametric models fail on heavily skewed targets.
*   **Mathematical Correction:** Applied a logarithmic transformation ($y_{new} = \log(y)$) to stabilize variance. This simple mathematical adjustment fundamentally boosted baseline model convergence and error minimization.
</details>

<details>
<summary><b>🤖 Phase 4: Machine Learning & Pipeline Architecture</b></summary>
<br>

*   Built an elegant, clean pre-processing pipeline mapping categorical variables seamlessly.
*   Utilized **Scikit-Learn** estimators to construct comparative analytics frameworks targeting minimum Mean Absolute Error (MAE) and maximum $R^2$ performance metrics.
</details>

---

## 🗺️ Architectural Data Flow & Feature Mapping
This blueprint illustrates how raw unstructured string properties inside `laptop_data.csv` are structurally decoded into clean numeric matrices:

```text
📥 Raw Row: "Apple MacBook Pro | 8GB | 128GB SSD | IPS Panel Retina Display 2560x1600"
      │
      ├── [Text Mining] ───────► RAM_GB = 8  (Continuous Numeric)
      ├── [Regex Engine] ──────► Is_IPS = 1  (Binary Boolean)
      ├── [Feature Splitting] ─► Width = 2560 , Height = 1600 (Numeric Space)
      └── [Categorical Map] ───► CPU_Brand = "Intel Core i5" (Encoded Performance Group)
                                      │
                                      ▼
                        [ Log-Transformed Regression ]
                                      │
                                      ▼
                     🎯 [ OPTIMIZED PRICE PREDICTION ]
