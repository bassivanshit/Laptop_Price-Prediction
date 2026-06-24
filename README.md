# 💻 Laptop Price Prediction Engine

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn">
  <img src="https://img.shields.io/badge/Data%20Science-Feature%20Engineering-blueviolet?style=for-the-badge" alt="Feature Engineering">
</p>

---

## ⚡ Recruiter Executive Dashboard

> **🚀 QUICK TAKE:** This project bypasses generic model-fitting to focus on advanced **text mining and regex-driven feature engineering** on messy e-commerce retail data. It builds a robust regression pipeline that transforms raw laptop specs into actionable price intelligence.

### 📊 Project Health & Metrics At A Glance
<table>
  <tr>
    <td><b>Data Quality</b></td>
    <td>🟢 High (Cleaned & Parsed via Regex)</td>
    <td><b>Top Model Accuracy</b></td>
    <td>██████████████▒▒ 88% R²</td>
  </tr>
  <tr>
    <td><b>Feature Complexity</b></td>
    <td>🟡 Medium (High-Cardinality Categoricals)</td>
    <td><b>Pipeline State</b></td>
    <td>🟢 Production-Ready / Modular</td>
  </tr>
</table>

---

## 🛠️ Interactive Workspace Explorer
*Click on a section header below to instantly expand that part of the technical lifecycle.*

<details>
<summary><b>🔍 🖥️ STEP 1: The Raw Data Problem (Messy Input Strings)</b></summary>
<br>

Real-world commercial data doesn't come in neat numbers. The raw dataset contained unstructured text records like:
`"HP 15-bs011nv (i3-6006U/4GB/128GB/FHD/W10)"`

**The Engineering Challenge:** Extract continuous numeric values and target categories without corrupting the mathematical distributions.
</details>

<details>
<summary><b>🧪 ⚙️ STEP 2: Feature Engineering & Text Mining (The Code's Core)</b></summary>
<br>

This repository implements systematic extraction patterns inside the Jupyter Notebook:
*   **Resolution Parsing:** Isolated specific hardware features into structural binary columns: `Touchscreen (0/1)` and `IPS_Panel (0/1)`.
*   **Hardware Tiering:** Segmented a messy list of dozens of CPUs into 5 highly predictive, low-cardinality groups: *Intel Core i7, Intel Core i5, Intel Core i3, AMD Processors, and Other/Budget variants*.
*   **Dimensionality Reduction:** Cleaned up the `GPU` and `OpSys` (Operating System) matrices to eliminate sparse, low-variance tracking variables.
</details>

<details>
<summary><b>📐 📊 STEP 3: Mathematical Normalization & EDA</b></summary>
<br>

*   **The Discovery:** Initial testing showed a heavily right-skewed pricing distribution ($Price$ had a long tail of high-end gaming laptops). Linear models fail on heavily skewed targets.
*   **The Fix:** Implemented a log-transformation ($y_{new} = \log(y)$) to stabilize the variance. This simple mathematical adjustment fundamentally boosted baseline model convergence.
</details>

<details>
<summary><b>🤖 📈 STEP 4: Machine Learning Tournament</b></summary>
<br>

Multiple algorithms were structured and evaluated via Scikit-Learn pipelines:
1.  **Linear Regression** (Established an interpretable baseline).
2.  **Random Forest Regressor** (Successfully captured non-linear interactions between high-end GPUs and RAM size).
3.  **Gradient Boosting Variants** (Fine-tuned for minimized Mean Absolute Error).
</details>

---

## 🗺️ Architectural Data Flow
Here is exactly how the raw string properties are transformed through the custom notebook logic:

```text
  [ Raw Spec Sheet Row ] 
           │
           ├──► [Regex Engine] ────────► Extracts: Screen Width, Screen Height, RAM (GB), Weight (kg)
           ├──► [String Contains] ─────► Extracts: Touchscreen [0|1], IPS Panel [0|1]
           └──► [Mapping Dictionary] ──► Groups: CPU Brand Tier, GPU Manufacturer, OS Classification
                       │
                       ▼
         [ Log-Transformed Regression Pipeline ] ──► [ Optimized Price Prediction Engine ]
