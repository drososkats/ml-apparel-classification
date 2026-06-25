# 📂 Dataset Information & Source

[![Kaggle](https://img.shields.io/badge/Kaggle-Fashion--MNIST-20BEFF?style=flat&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/zalando-research/fashionmnist)

This directory is reserved for the **Fashion-MNIST** dataset used to train and evaluate the machine learning model. To preserve repository cleanliness and comply with version control best practices, the actual large CSV files are excluded from this repository via `.gitignore` and must be downloaded locally.

---

## 🔗 Official Download Link

The dataset is publicly available and can be downloaded from Kaggle:

* **Dataset URL:** [Fashion-MNIST Dataset on Kaggle](https://www.kaggle.com/datasets/zalando-research/fashionmnist)

---

## 📝 Expected Directory Structure

After downloading the dataset, extract the contents and place the raw CSV files directly into this `dataset/` folder. For the scripts and notebooks to run correctly, the directory must be structured exactly as follows:

```text
dataset/
├── README.md                  <-- This file
├── fashion-mnist_train.csv    <-- The training set (60,000 samples)
└── fashion-mnist_test.csv     <-- The testing set (10,000 samples)
```

---

## 🧾 Dataset Properties

**Format:** Each row represents a single image. The first column is the label (class ID from 0 to 9), and the remaining 784 columns represent the 28×28 grayscale pixel intensities (values from 0 to 255).

**Classes:** The 10 clothing categories are perfectly balanced (6,000 training samples per class):

| Label | Class       |
|:-----:|:------------|
| 0     | T-shirt/top |
| 1     | Trouser     |
| 2     | Pullover    |
| 3     | Dress       |
| 4     | Coat        |
| 5     | Sandal      |
| 6     | Shirt       |
| 7     | Sneaker     |
| 8     | Bag         |
| 9     | Ankle boot  |