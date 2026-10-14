# 🌱 Dry Bean Classification — Machine Learning

A machine learning project that classifies dry beans into seven varieties using numerical features extracted from bean images. The project explores **Decision Trees, Ensemble Learning, Hyperparameter Tuning, PCA, and Feature Selection** to compare model performance.

## 📌 Project Overview

The goal is to predict the variety of a dry bean using its physical measurements, such as area, perimeter, compactness, and axis lengths.

The project compares different machine learning algorithms and investigates how dimensionality reduction and feature selection affect classification performance.

## 📊 Dataset

- **Source:** [UCI Dry Bean Dataset](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset)
- **Original dataset:** 13,611 samples
- **Samples after cleaning:** 13,543
- **Features:** 16 numerical features
- **Target:** `Class`
- **Number of classes:** 7

The seven bean varieties are:

- Barbunya
- Bombay
- Cali
- Dermason
- Horoz
- Seker
- Sira

## ✨ Key Features

- 🧹 **Data Preprocessing:** Checked for missing values and duplicate rows.
- 📈 **Exploratory Data Analysis:** Visualized feature relationships and correlations.
- 🌳 **Decision Trees:** Explored tree visualization, different splitting criteria, maximum depth, and cost-complexity pruning.
- 🧩 **Bagging:** Compared Bagged SVM and Bagged Decision Tree models.
- 🌲 **Random Forest:** Tuned the number of estimators and the number of features considered at each split.
- 🚀 **Boosting:** Experimented with Gradient Boosting and XGBoost.
- 📉 **PCA:** Reduced dimensionality while retaining at least 95% of the training data's variance.
- 🎯 **Feature Selection:** Selected the six most important original features using Random Forest feature importance.
- 📏 **Model Evaluation:** Compared accuracy, weighted precision, weighted recall, weighted F1-score, and confusion matrices.

## ⚙️ Project Workflow

1. Load the dataset and clean the data.
2. Separate the numerical features from the target class.
3. Split the data into training and testing sets using an 80/20 split.
4. Explore feature distributions, relationships, and correlations.
5. Train and tune Decision Tree models.
6. Compare bagging, Random Forest, Gradient Boosting, and XGBoost.
7. Evaluate the models using classification metrics.
8. Apply PCA and select the six most important features.
9. Compare the original features, PCA components, and selected features.

## 🛠️ Technologies Used

- **Python** — Main programming language
- **Pandas & NumPy** — Data manipulation and numerical operations
- **Matplotlib & Seaborn** — Data visualization
- **Scikit-learn** — Machine learning, preprocessing, PCA, and evaluation
- **XGBoost** — Gradient-boosted decision trees
- **Jupyter Notebook** — Development and experimentation

## 🏆 Results

The recorded final comparison produced the following results:

| Feature Representation | Accuracy | Weighted F1-Score |
|---|---:|---:|
| Original 16 features | 92.36% | 92.36% |
| PCA: 4 components | 89.59% | 89.53% |
| Selected 6 features | 90.99% | 91.00% |

The original-feature model achieved the highest recorded performance. PCA reduced the input to four components while retaining at least 95% of the variance, whereas feature selection retained six interpretable original features with a smaller decrease in performance.

The notebook also reports **91.99% accuracy for XGBoost** among the boosting models tested. The results above represent the final comparison using the selected best-performing model and different feature representations.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/dry-bean-classification.git
cd dry-bean-classification
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Create a virtual environment (optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install the dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the notebook

Open the project notebook using Jupyter Notebook or JupyterLab:

```bash
jupyter notebook
```

Run the cells in order to reproduce the preprocessing, model training, evaluation, and feature-reduction experiments.

## 📁 Repository Structure

```text
dry-bean-classification/
├── README.md
├── requirements.txt
├── .gitignore
└── Dry_Bean_Classification_Project.ipynb
```

## 🔮 Possible Improvements

- Use cross-validation for more reliable model comparisons.
- Tune hyperparameters using a validation set or cross-validation.
- Add more detailed per-class performance analysis.
- Save the final trained model for reuse.
- Build a simple interface that predicts bean varieties from numerical measurements.

## 🙌 Acknowledgements

- [UCI Machine Learning Repository — Dry Bean Dataset](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)

---

*This project was developed for educational purposes to explore classification algorithms, ensemble learning, and feature reduction.*
