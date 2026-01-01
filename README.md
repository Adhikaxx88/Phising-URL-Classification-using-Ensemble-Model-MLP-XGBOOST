# Phising-URL-Classification-using-Ensemble-Model
This project detects phishing URLs using a high-performance Stacking Ensemble (XGBoost + MLP) optimized for GPU. By combining robust lexical features with Sentence-BERT (SBERT) embeddings, the model achieves superior accuracy in identifying malicious links.
# 🛡️ Phishing URL Classification: Stacking Ensemble

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-SBERT-ee4c2c)
![XGBoost](https://img.shields.io/badge/XGBoost-GPU-green)
![Status](https://img.shields.io/badge/Status-Active-success)

This project detects phishing URLs using a high-performance **Stacking Ensemble** (XGBoost + MLP) optimized for GPU. By combining robust lexical features with **Sentence-BERT (SBERT)** embeddings, the model achieves superior accuracy in identifying malicious links.

## 🚀 Key Features

* **Hybrid Feature Engineering**: Merges traditional lexical features (URL length, entropy, etc.) with deep semantic features using `sentence-transformers` (SBERT).
* **Stacking Architecture**:
    * **Level-0 (Base)**: GPU-accelerated **XGBoost** and **MLP** (with PCA).
    * **Level-1 (Meta)**: **MLP Classifier** to aggregate predictions.
* **GPU Acceleration**: Fully optimized for CUDA-enabled devices to handle large datasets efficiently.
* **Advanced Preprocessing**: Utilizes a robust pipeline of Scalers (Robust, Standard, MinMax) tailored to feature distributions.

## 🛠️ Tech Stack

* **Language**: Python
* **Embeddings**: Sentence-BERT (`all-mpnet-base-v2`)
* **Models**: XGBoost, Scikit-Learn (MLP, StackingClassifier)
* **Tuning**: RandomizedSearchCV

## 📂 Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/AdhikaGunawan/phishing-url-classification-stacking-ensemble.git](https://github.com/AdhikaGunawan/phishing-url-classification-stacking-ensemble.git)
    cd phishing-url-classification-stacking-ensemble
    ```

2.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

## 💻 Usage

1.  Prepare your dataset (ensure `train.csv` and `test.csv` are in the root directory).
2.  Run the training script:
    ```bash
    python train_model.py
    ```

## 📊 Performance

* **Metric**: AUROC (Area Under ROC Curve)
* **Validation Score**: **~0.995** (State-of-the-art performance)

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

---
*Created by [Adhika Gunawan](https://github.com/AdhikaGunawan)*
