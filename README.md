# 💻 Laptop Price Prediction Engine

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/Data%20Visualization-Seaborn%20%2F%20Matplotlib-11557C?style=for-the-badge&logo=pandas&logoColor=white" alt="Visualization">
  <img src="https://img.shields.io/badge/Lifecycle-End--to--End%20Pipeline-success?style=for-the-badge" alt="Pipeline">
</p>

> **Recruiter Quick Summary:** This repository demonstrates an end-to-end Data Science pipeline that extracts raw text features from dynamic e-commerce laptop specifications (e.g., CPU, Screen Resolution, RAM) and transforms them into an optimized pricing engine.

---

## 🧭 Live Interactive Project Pipeline
*Click on any phase below to expand the engineering deep-dive and see exactly how the code was implemented.*

<details>
<summary><b>🧹 Phase 1: Advanced Data Cleaning & Text Mining</b></summary>
<br>

*   **Noise Reduction:** Stripped static text flags (`GB`, `kg`) from numerical variables to transform them into raw statistical continuous datatypes.
*   **Handling Nulls & Anomalies:** Verified dataset integrity by parsing complex structural strings down to uniform baselines.
</details>

<details>
<summary><b>⚙️ Phase 2: Strategic Feature Engineering (The Core Highlight)</b></summary>
<br>

*   **Display Resolution Extraction:** Used string filtering to identify hidden categorical variables: **Touchscreen Capability (0/1)** and **IPS Panel Integration (0/1)**.
*   **Hardware Architecture Segmentation:** 
    *   Mapped high-cardinality Central Processing Units (CPUs) into 5 major core performance groups (Intel Core i3, i5, i7, AMD, and Other variants).
    *   Segmented Graphic Processing Units (GPUs) by brand equity to eliminate model bias.
</details>

<details>
<summary><b>📊 Phase 3: Exploratory Data Analysis & Feature Insights</b></summary>
<br>

*   Identified that the target variable (`Price`) was heavily right-skewed.
*   **Mathematical Correction:** Applied a logarithmic transformation ($y = \log(x)$) to normalize the distribution, ensuring optimal convergence for the linear and ensemble regression structures.
</details>

<details>
<summary><b>🤖 Phase 4: Pipeline Architecture & Modeling</b></summary>
<br>

*   Built an elegant, production-ready pre-processing pipeline mapping categorical variables seamlessly.
*   Utilized **Scikit-Learn** estimators to construct comparative analytics frameworks targeting minimum Mean Absolute Error (MAE).
</details>

---

## 📈 Feature Mapping Architecture
This blueprint illustrates how complex text strings inside `laptop_data.csv` were structurally decoded into high-value numeric matrices:

```text
📥 Raw Row: "Apple MacBook Pro | 8GB | 128GB SSD | IPS Panel Retina Display 2560x1600"
      │
      ├── [Text Mining] ───────► RAM_GB = 8  (Continuous)
      ├── [Regex Engine] ──────► Is_IPS = 1  (Binary Boolean)
      ├── [Feature Splitting] ─► Width = 2560 , Height = 1600 (Numeric)
      └── [Categorical Map] ───► CPU_Brand = "Intel Core i5" (Encoded Group)
