# Predicting Option Prices: From the Black-Scholes Model to Advanced Machine Learning Methods

This project explores option pricing using both traditional financial models and modern machine learning techniques. Originally conducted as part of the STP 550 course at Arizona State University, the study evaluates and compares models such as the Black-Scholes formula, decision trees, random forests, gradient boosting, and neural networks.

📄 **Report**: [ProjectReport.pdf](./ProjectReport.pdf)  
📓 **Notebook**: See the included `.ipynb` file(s) for code implementations and experiments.

---

## 📌 Overview

Traditional models like Black-Scholes rely on strict assumptions such as constant volatility and frictionless markets. However, real-world data often violates these assumptions. This project demonstrates how machine learning models—free from such constraints—can outperform the Black-Scholes model in pricing American-style options.

---

## 🧠 Methods

### ✅ Classical Model
- **Black-Scholes**: Analytical pricing formula for European call options based on geometric Brownian motion.

### ✅ Machine Learning Models
- **Decision Tree**
- **Random Forest**
- **Gradient Boosting**
- **Neural Networks (NN1 in TensorFlow, NN2 in PyTorch)**

Features used:
- Moneyness
- Time to expiry
- Implied volatility
- Polynomial expansions (in NN2)

---

## 📈 Data

Data were sourced from **OptionMetrics via WRDS**, focusing on US-listed options. Due to availability, the main analysis focuses on **American-style options** (~36,000 data points), with **European-style options** (~8,000 points) used for supplemental analysis.

---

## 🧪 Results

### Model Performance (RMSE):
| Model             | RMSE    |
|------------------|---------|
| Random Forest     | **43.88** |
| Neural Network (NN2) | 49.68  |
| Gradient Boosting | 54.67  |
| Decision Tree     | 60.97  |

- Neural networks reduced prediction error by **~6×** compared to Black-Scholes (MSE: 2053 vs 11458).
- Random forests and neural networks showed the best performance across varying market conditions.

---

## 🔮 Future Work

- Explore advanced architectures (e.g., RNNs, Transformers) to capture time dependencies.
- Incorporate bid-ask spread modeling for deeper market insight.
- Analyze European-style options in more detail with expanded datasets.

---

## 🛠️ Getting Started

### Requirements
- Python 3.x
- Jupyter Notebook
- `numpy`, `scikit-learn`, `matplotlib`, `torch`, `tensorflow`, etc.

Install dependencies:

```bash
pip install -r requirements.txt
