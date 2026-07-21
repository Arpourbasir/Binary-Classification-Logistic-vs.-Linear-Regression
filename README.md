# 📈 Regression vs. Classification Analysis
### Linear Regression vs. Logistic Regression for Binary Classification

A machine learning project that compares **Linear Regression** and **Logistic Regression** when applied to a **binary classification** problem. The objective is to demonstrate why Logistic Regression is fundamentally more suitable for classification tasks and how Linear Regression is affected by outliers.

This project was developed for the **Introduction to Data Mining** course at **K. N. Toosi University of Technology (KNTU)**.

---

# 📖 Project Overview

Although **Linear Regression** is designed for predicting continuous values, it is sometimes incorrectly applied to binary classification by thresholding its outputs (e.g., at 0.5).

This project compares Linear Regression with Logistic Regression using a synthetic dataset specifically designed to highlight the weaknesses of Linear Regression in classification problems.

The comparison includes:

- Model training
- Decision boundary visualization
- Classification accuracy
- Outlier sensitivity analysis

---

# ✨ Features

- 📈 Linear Regression implementation using Scikit-Learn
- 📊 Logistic Regression implementation
- 🎯 Binary classification comparison
- 📉 Decision boundary visualization
- ⚖️ Accuracy evaluation
- 🚨 Outlier sensitivity analysis
- 🧠 Sigmoid probability interpretation
- 📚 Educational comparison of regression and classification models

---

# 📂 Project Structure

```text
Regression-vs-Classification/
│
├── Regression_vs_Classification.ipynb    # Main notebook
├── README.md                             # Project documentation
└── requirements.txt                      # Dependencies (optional)
```

---

# 📊 Dataset

A small synthetic one-dimensional dataset is used to clearly illustrate the behavioral differences between the two algorithms.

| Feature (X) | Target (y) |
|------------:|-----------:|
| 4.5 | 0 |
| -4.0 | 0 |
| 3.5 | 0 |
| -3.0 | 0 |
| 2.5 | 0 |
| -2.0 | 1 |
| 1.5 | 1 |
| -1.0 | 1 |
| 0.5 | 1 |
| **20.0** | **1 (Outlier)** |

The value **20.0** is intentionally included as an extreme outlier.

---

# 🏗 Methodology

The project follows these steps:

1. Construct the dataset.
2. Train a Linear Regression model.
3. Train a Logistic Regression model.
4. Generate predictions.
5. Apply a classification threshold for Linear Regression.
6. Evaluate classification accuracy.
7. Visualize both decision boundaries.
8. Analyze the effect of the outlier.

---

# 📈 Linear Regression

Linear Regression predicts continuous values:

\[
\hat{y}=wX+b
\]

To perform classification, predictions are converted into class labels using a threshold:

```text
Prediction ≥ 0.5 → Class 1
Prediction < 0.5 → Class 0
```

However, Linear Regression is **not designed for classification**, making it vulnerable to outliers and producing unbounded outputs.

---

# 📊 Logistic Regression

Logistic Regression models probabilities using the sigmoid function:

\[
\sigma(z)=\frac{1}{1+e^{-z}}
\]

Its output is always between **0 and 1**, allowing predictions to be interpreted as probabilities.

Classification is performed using:

```text
Probability ≥ 0.5 → Class 1
Probability < 0.5 → Class 0
```

---

# ⚖️ Comparison

| Property | Linear Regression | Logistic Regression |
|-----------|-------------------|---------------------|
| Designed for Classification | ❌ | ✅ |
| Probability Output | ❌ | ✅ |
| Robust to Outliers | ❌ | ✅ |
| Decision Boundary | Linear Threshold | Sigmoid |
| Output Range | (-∞, +∞) | [0, 1] |
| Loss Function | Mean Squared Error | Log Loss |

---

# 🚨 Effect of Outliers

The synthetic dataset contains an extreme point:

```text
X = 20
```

This point significantly affects the Linear Regression line by pulling it toward the outlier.

As a result:

- Decision boundary shifts.
- Classification accuracy decreases.
- Normal samples may be misclassified.

Logistic Regression remains considerably more stable because it optimizes **Log Loss** rather than **Mean Squared Error**.

---

# 📊 Model Evaluation

The models are evaluated using:

- Classification Accuracy
- Decision Boundary Visualization

Linear Regression predictions are converted into class labels using a threshold of **0.5**.

---

# 🚀 Getting Started

## Requirements

- Python 3.9+
- Jupyter Notebook

---

## Required Libraries

```text
numpy
pandas
matplotlib
scikit-learn
```

Install dependencies:

```bash
pip install numpy pandas matplotlib scikit-learn
```

---

# ▶️ Running the Project

Clone the repository:

```bash
git clone https://github.com/your-username/Regression-vs-Classification.git
```

Navigate to the project directory:

```bash
cd Regression-vs-Classification
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Regression_vs_Classification.ipynb
```

Run all notebook cells.

---

# 📉 Expected Results

The project demonstrates that:

- Logistic Regression achieves a more reliable decision boundary.
- Linear Regression is heavily influenced by extreme values.
- Logistic Regression provides meaningful probability estimates.
- Logistic Regression is the preferred choice for binary classification tasks.

---

# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Programming Language |
| NumPy | Numerical Computing |
| Pandas | Dataset Handling |
| Matplotlib | Data Visualization |
| Scikit-Learn | Machine Learning Models |
| Jupyter Notebook | Interactive Development |

---

# 🎯 Learning Outcomes

This project demonstrates practical understanding of:

- Linear Regression
- Logistic Regression
- Binary Classification
- Regression vs. Classification
- Decision Boundaries
- Sigmoid Function
- Outlier Analysis
- Model Evaluation
- Scikit-Learn

---

# 🔮 Future Improvements

Potential future enhancements include:

- 📈 Precision, Recall, and F1-Score evaluation
- 📊 ROC Curve and AUC analysis
- 📉 Confusion Matrix visualization
- 🎨 Interactive decision boundary plots
- 🔄 Comparison with Support Vector Machines (SVM)
- 🌲 Decision Tree comparison
- 🤖 Neural Network implementation
- 📦 Hyperparameter tuning

---

# 📚 Academic Information

**Course**

Introduction to Data Mining

**University**

K. N. Toosi University of Technology (KNTU)

**Semester**

Fall 2024

---

# 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.

Feel free to fork the repository and submit a Pull Request.

---

# 📄 License

This project was developed for educational purposes as part of a university assignment.

You are free to study, modify, and extend the project for learning and research purposes.

---

# 👨‍💻 Arpourbasir

**Alireza Pourbasir**

GitHub: https://github.com/Arpourbasir
---

⭐ If you found this project useful, consider giving it a **Star ⭐** on GitHub!
