# Climate Trend Analysis & Predictive Modeling 🌦️

A comprehensive time-series analysis and forecasting system designed to study climate patterns, evaluate statistical significance in long-term changes, and predict key meteorological variables (Rainfall, Minimum Temperature, and Maximum Temperature).

This project cleans historical tabular climate datasets, checks for historical shifts using monotonic trend assessments, and structures data partitions for time-series forecasting models.

--

## 🚀 Features

- **Data Wrangling & Normalization**: Automated extraction and structural re-indexing of noisy multi-column Excel spreadsheets into machine-learning-ready time series frames.
- **Mann-Kendall Trend Assessment**: Employs non-parametric statistical tests (`pymannkendall`) to quantify the statistical significance ($p$-values) and direction of monthly rainfall shifts over a 40+ year timeline.
- **Temporal Train/Validation Partitions**:
  - **Training Interval**: 1984 – 2000
  - **Validation Interval**: 2001 – 2023
  - **Target Prediction Window**: 2021 – 2024
- **Exploratory Visualizations**: Features advanced trend plots using `Seaborn` and `Matplotlib` to identify anomalous climate fluctuations.

---

## 🛠️ Technical Stack

- **Language**: Python
- **Data Engineering**: Pandas, NumPy
- **Statistical Analytics**: PyMannKendall
- **Data Visualization**: Matplotlib, Seaborn

---

## 📈 Methodology & Pipeline

### 1. Data Cleaning & Re-shaping
Historical meteorological worksheets often contain unindexed headers and structural noise. The preprocessing pipeline:
- Prunes isolated null structural blocks.
- Maps short-character representations to explicit monthly properties (`jan` through `dec`).
- Performs down-casting and data type coercion to float64 tensors for seamless matrix computations.

### 2. Monotonic Trend Evaluation
The **Mann-Kendall (MK) Test** determines if a variable has a monotonic upward or downward trend over time:

---

## ⚙️ Installation & Usage

1. **Clone the repository**:
```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   cd your-repo-name
