# Machine Learning Apparel Classification Pipeline

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA4F01.svg?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Fashion--MNIST-20BEFF?style=flat&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/zalando-research/fashionmnist)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Repo Size](https://img.shields.io/github/repo-size/drososkats/ml-apparel-classification)

A professional, end-to-end Machine Learning pipeline developed to classify apparel images using an optimized Support Vector Machine (SVM) model. Based on the comprehensive study conducted for Harokopio University of Athens, this repository demonstrates a structured data science workflow featuring exploratory data analysis, data normalization, advanced feature extraction, and systematic hyperparameter tuning.

---

## 📈 Executive Summary

* **Objective:** Automatically classify high-dimensional 28×28 grayscale images of clothing items into 10 distinct categories.
* **Core Architecture:** MinMaxScaler ➔ Principal Component Analysis (PCA) ➔ Support Vector Classifier (SVC) with RBF Kernel.
* **Final Performance:** Achieved a **91.0% overall accuracy** on the unseen test set, proving robust generalization capabilities.

---

## 🛠️ Pipeline Architecture

To mitigate the *Curse of Dimensionality* and improve computational efficiency, the dataset undergoes a rigorous preprocessing sequence:

1. **Feature Scaling:** Pixel intensities are rescaled from their original `[0, 255]` range to a normalized `[0, 1]` range using `MinMaxScaler`. This step ensures numerical stability and equal feature weight during geometric distance calculations.
2. **Dimensionality Reduction (PCA):** Principal Component Analysis is applied to compress the feature space from 784 raw pixels down to **188 principal components**. This retains **95% of the total explained variance** while filtering out background noise and vastly accelerating training times.
3. **Model Optimization:** A Support Vector Classifier (SVC) utilizing a **Radial Basis Function (RBF) Kernel** was selected to model non-linear decision boundaries. Hyperparameter tuning via Grid Search established the optimal regularization parameter at **$C \approx 3.22$**.

---

## 📂 Repository Layout

```text
ml-apparel-classification/
├── README.md                          <-- Technical documentation and overview
├── requirements.txt                   <-- Python dependencies and libraries
├── .gitignore                         <-- Directives to exclude local datasets and cache
├── notebooks/
│   └── apparel_mnist_pipeline.ipynb   <-- Structured exploratory analysis & model training
└── models/
    └── fashion_svm_pipeline.pkl       <-- Serialized, pre-trained model for external integration
```

---

## 🔍 Performance Insights

* **Dataset Balance:** The baseline dataset contains a perfectly symmetrical distribution across all target classes (6,000 samples per class), making classification accuracy a reliable performance metric.
* **Error Patterns:** Error analysis via the confusion matrix indicates near-perfect classification for highly distinct geometries (e.g., Trousers, Bags). Minor visual ambiguities remain between visually contiguous classes such as "Shirts" vs. "Coats".

---

## 💻 Setup and Local Replication

**1. Clone the Repository:**

```bash
git clone https://github.com/drososkats/ml-apparel-classification.git
cd ml-apparel-classification
```

**2. Install Dependencies:**

Before running the project, install the required Python libraries using `pip`:

```bash
pip install -r requirements.txt
```

**3. Execute the Pipeline:**

To step through the exploratory analysis, data preprocessing, and model training, launch Jupyter Lab or Jupyter Notebook in your environment:

```bash
jupyter lab
```

Then open `notebooks/apparel_mnist_pipeline.ipynb` and run the cells sequentially.