# Comparison between Manual Linear Regression and Library-based Implementation

## 📌 Overview
This project compares two approaches to implementing **Linear Regression**:

1. **Manual (from-scratch)** implementation using Gradient Descent and analytical formulas.  
2. **Library-based** implementation using Python’s `scikit-learn`.

We evaluate both methods on two real-world time series datasets:
- **Thermostat Sales** – weekly sales data.
- **Air Passengers** – monthly airline passenger counts.

The goal is to analyze performance, accuracy, computational cost, and applicability in different scenarios.

---

## 🎯 Objectives
- Present the basic theory of Linear Regression.
- Explain evaluation metrics: **MSE**, **RMSE**, and **R²**.
- Implement Linear Regression manually and using a library.
- Compare results on both datasets.
- Identify when each approach is more suitable.

---

## 📂 Datasets
| Dataset           | Samples | Time Unit | Features  | Description |
|-------------------|---------|-----------|-----------|-------------|
| Thermostat Sales  | 52      | Week      | 1 numeric | Weekly thermostat sales counts. |
| Air Passengers    | 144     | Month     | 1 numeric | Monthly airline passenger counts. |

Both datasets are clean, numeric, and preprocessed for training.

---

## ⚙ Methodology
1. **Data Preprocessing**
   - Normalize and reshape data.
   - Train/Test split: 80% / 20%.

2. **Manual Linear Regression**
   - Implemented with NumPy.
   - Parameters:
     - Learning rate: `0.0001`
     - Epochs: `100,000`
   - Loss function: **MSE**.

3. **Library-based Linear Regression**
   - Implemented with `sklearn.linear_model.LinearRegression`.
   - Auto-optimized parameters.

4. **Evaluation**
   - Compare **MSE**, **RMSE**, and **R²**.
   - Visualize regression lines on train and test sets.

---

## 📊 Results Summary

### Thermostat Sales
| Method  | MSE    | RMSE   | R²     |
|---------|--------|--------|--------|
| Manual  | 755.11 | 27.48  | 0.722  |
| Library | 783.88 | 28.00  | 0.711  |

**Observation:** Both methods perform very similarly.

---

### Air Passengers
| Method  | MSE      | RMSE    | R²       |
|---------|----------|---------|----------|
| Manual  | 12368.72 | 111.21  | -0.1135  |
| Library | 12311.83 | 110.96  | -0.1084  |

**Observation:** Both models fail to capture the trend due to seasonality and non-linearity.

---

## 🏁 Conclusions
- **Thermostat Sales**: Good performance due to clear linear trend.
- **Air Passengers**: Poor performance due to seasonal and non-linear patterns.
- **Manual implementation**:
  - Good for learning and understanding the algorithm.
  - Slower, requires manual tuning.
- **Library implementation**:
  - Faster, optimized, user-friendly.
  - Ideal for practical applications.

---

## 🛠 Technologies Used
- Python 3.x
- NumPy
- Pandas
- Matplotlib
- scikit-learn

---

## 🚀 How to Run
```bash
# Clone repository
git clone https://github.com/Desuuy/Comparison-between-Manual-Linear-Regression-and-Library-based-Implementation.git
cd Comparison-between-Manual-Linear-Regression-and-Library-based-Implementation

# Install dependencies
pip install -r requirements.txt


