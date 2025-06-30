# GAN-CatBoost-SHAP: An Interpretable Hybrid Framework for Anomaly Detection in IoMT Networks

## 🔍 Description
This project presents a reproducible AI Application for anomaly detection in Internet of Medical Things (IoMT) networks. It combines:
- **GAN (Generative Adversarial Networks)** for data augmentation
- **CatBoost** for classification
- **SHAP** for interpretability

The entire code is written in **Google Colab**, and the dataset used is **CICIoMT2024**.

## 📦 Dataset Information
- **Name:** CICIoMT2024 Dataset  
- **Source:** [CIC IoMT 2024 – Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/iomt-dataset-2024.html)  
- **Description:** A labeled dataset containing normal and malicious IoMT network traffic data. The dataset must be requested from the official site for access.  
- **Usage:** After download, upload the `.csv` file manually into Colab when running the notebook.

## 🧠 Code Information
- **Colab notebook link:** [Open in Google Colab](https://colab.research.google.com/drive/1-UVsxg6r-xQDj2HGreNUKjR1mvtlofdu?usp=sharing)
- The notebook includes:
  - Data preprocessing and cleaning
  - GAN-based data augmentation
  - CatBoost model training
  - SHAP visualizations for interpretability
- No external scripts are required — all code is included in a single `.ipynb` file.

## 🚀 Usage Instructions
1. Open the notebook in [Google Colab](https://colab.research.google.com/drive/1-UVsxg6r-xQDj2HGreNUKjR1mvtlofdu?usp=sharing).
2. Download the dataset from the CIC website and upload it in the runtime.
3. Run all cells in sequence:
   - Preprocessing
   - GAN training and augmentation
   - CatBoost model training
   - SHAP explanation
4. Review final results and visualizations in the notebook.

## 📚 Requirements
Run this in Colab and install dependencies using:
``python
!pip install catboost shap pandas numpy matplotlib scikit-learn

## 📊 Methodology

### Data Processing
- Loaded and cleaned CICIoMT2024 dataset
- Normalized features
- Handled class imbalance using GAN-based augmentation

### Model Training
- CatBoost used for binary classification
- Both baseline and GAN-augmented datasets evaluated
- Hyperparameter tuning applied for optimal performance

### Interpretability
- SHAP values computed to explain model predictions
- Visualizations highlight top features contributing to anomaly detection

---

## 💻 Computing Infrastructure
- Platform: Google Colab
- OS: Linux (Colab backend)
- RAM: 12–16 GB (standard Colab runtime)
- GPU: Optional (used for GAN training)
- Python Version: 3.10

---

## 🧪 Evaluation Method

Model performance was evaluated by comparing:

- **Baseline:** CatBoost trained on original dataset  
- **Hybrid:** CatBoost trained on GAN-augmented dataset

### Metrics Used
- Accuracy  
- Precision  
- Recall  
- F1-Score  

> Metrics were calculated per attack type and averaged across runs.  
> GAN-based augmentation improved minority class detection significantly.

---

## 🚧 Limitations
- GAN-generated data may introduce noise if not properly trained
- Framework is currently specific to the CICIoMT2024 dataset and may require adjustments for general use
- SHAP computation can be resource-intensive on large datasets

---

## 📌 Note
All code was implemented in a single `.ipynb` notebook and is intended for academic and research use only.
