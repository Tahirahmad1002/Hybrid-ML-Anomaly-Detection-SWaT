# Hybrid Machine Learning Approach for Anomaly Detection in Cyber-Physical Systems

![python](https://img.shields.io/badge/python-3.8+-blue)
![machine-learning](https://img.shields.io/badge/machine-learning-cps-green)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([PASTE_YOUR_COLAB_LINK_HERE](https://colab.research.google.com/drive/1mpOeOE1nDhgYZyYTpY0CqC-lafnftKh1?usp=sharing))

---

## 📌 Project Overview

This repository implements a **hybrid machine learning anomaly detection system** for **Cyber-Physical Systems (CPS)** using the **SWaT dataset**.  

The system combines:  
- **Random Forest (RF)** → detects **known attacks**  
- **LSTM Autoencoder (LSTM-AE)** → detects **unknown anomalies**  
- **Hybrid Fusion Strategy** → combines both models for better reliability  

The project is implemented in **Python** using **Google Colab**, and demonstrates high performance in industrial control anomaly detection.

---

## 🎯 Problem Motivation

Cyber-Physical Systems like water treatment plants are critical infrastructure. A single anomaly can cause:  
- **Water contamination**  
- **Equipment damage**  
- **Service disruption**  

Traditional detection systems face challenges like:  
- **Class imbalance**  
- **Temporal dependencies**  
- **Zero-day attacks**  

The hybrid approach addresses these challenges effectively.

---

## 📊 Dataset Description

**Dataset:** Secure Water Treatment (SWaT)  
**Key Characteristics:**  
- 51 sensor & actuator features  
- 11 days of continuous operation  
- 36 cyber-attack scenarios  
- Binary labels: `0` → Normal, `1` → Attack  
- Highly imbalanced (~88% normal, ~12% attack)

> ⚠️ Note: SWaT dataset is **not included** in this repository. You must request access officially.

---

## 🧠 Methodology

1. **Data Preprocessing**
   - Missing value handling  
   - Min–Max normalization  
   - Feature selection & train-test split (70% / 30%)

2. **Random Forest Classifier (Supervised)**
   - Captures known attack patterns  
   - Handles high-dimensional features  
   - Robust to class imbalance

3. **LSTM Autoencoder (Unsupervised)**
   - Trained only on **normal sequences**  
   - Detects anomalies via **reconstruction error**  

4. **Hybrid Fusion Strategy**
   - Combines **RF predictions** and **AE reconstruction error**  
   - Reduces false negatives

---

## 🧪 Experimental Results

**Performance Metrics:**

| Model            | Accuracy | Precision | Recall | F1-Score |
|------------------|----------|-----------|--------|----------|
| Random Forest    | 92%      | 90%       | 88%    | 89%      |
| LSTM Autoencoder | 95%      | 93%       | 94%    | 93%      |
| **Hybrid Model** | **97%**  | **96%**   | **97%**| **96%**  |

**Observations:**  
- RF is strong on known attacks  
- LSTM-AE captures unseen anomalies  
- Hybrid model outperforms both  

---

## 📂 Repository Structure

Hybrid-ML-Anomaly-Detection-SWaT/
│
├── notebook/
│ └── Hybrid_ML_Anomaly_Detection_SWaT.ipynb
├── report/
│ └── Hybrid_ML_Anomaly_Detection_SWaT.pdf
├── results/
│ ├── accuracy_plot.png
│ └── confusion_matrix.png
├── requirements.txt
└── README.md

yaml
Copy code

---

## ▶️ How to Run

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/Hybrid-ML-Anomaly-Detection-SWaT.git
cd Hybrid-ML-Anomaly-Detection-SWaT
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the notebook in Jupyter or Google Colab:

Open notebook/Hybrid_ML_Anomaly_Detection_SWaT.ipynb

Run all cells sequentially

⚙️ Requirements
Python 3.8+

Libraries:

numpy, pandas, matplotlib, seaborn

scikit-learn

tensorflow, keras

All dependencies are listed in requirements.txt.

🚀 Future Improvements
Real-time anomaly detection

Explainable AI (SHAP)

Deployment on edge devices / PLCs

Evaluation on additional CPS datasets

Transformer-based models for better temporal analysis

👨‍💻 Author
Tahir Ahmad
Software Engineering Student | AI & Cybersecurity

📜 License
This project is for educational and internship purposes.
Free to use and modify with proper attribution.

⭐ If you find this project helpful, please give it a star!
