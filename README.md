
Hybrid Machine Learning Approach for Anomaly Detection in Cyber-Physical Systems
[![open in colab](https://colab.research.google.com/assets/colab-badge.svg)]([LINK_TO_NOTEBOOK](https://colab.research.google.com/drive/1mpOeOE1nDhgYZyYTpY0CqC-lafnftKh1?usp=sharing))
![python](https://img.shields.io/badge/python-3.8+-blue)
![machine-learning](https://img.shields.io/badge/machine-learning-cps-green)

📌 Project Overview

This repository presents a hybrid machine learning–based anomaly detection system for Cyber-Physical Systems (CPS) using the Secure Water Treatment (SWaT) dataset.
The project combines supervised and unsupervised learning techniques to detect both known cyber-attacks and previously unseen (zero-day) anomalies in industrial control systems.

The hybrid approach integrates:

Random Forest (RF) for detecting known attack patterns

LSTM Autoencoder (LSTM-AE) for detecting unknown anomalies through reconstruction error

A fusion strategy to improve robustness and reduce false negatives

This work was implemented and executed using Google Colab, and the results demonstrate that the hybrid model outperforms individual models.

🎯 Problem Motivation

Cyber-Physical Systems such as water treatment plants are critical infrastructures.
A successful cyber attack can lead to:

Water contamination

Equipment damage

Public safety risks

Large-scale service disruption

Traditional detection systems struggle with:

Class imbalance

Temporal dependencies

Novel (unseen) attacks

This project addresses these challenges using a hybrid ML approach.

📊 Dataset Description

Dataset: Secure Water Treatment (SWaT)
Developed by: Singapore University of Technology and Design (SUTD)

Key characteristics:

51 sensor and actuator features

Time-series industrial data

11 days of continuous operation

36 cyber-attack scenarios

Binary labels:

0 → Normal

1 → Attack

Highly imbalanced dataset (~88% normal, ~12% attack)

⚠️ Note:
The SWaT dataset is restricted and not included in this repository.
Users must request access from the official source.

🧠 Methodology

The project follows a structured machine learning pipeline:

1️⃣ Data Preprocessing

Handling missing values

Min–Max normalization

Feature scaling

Stratified train–test split (70% / 30%)

2️⃣ Random Forest Classifier (Supervised)

Learns from labeled attack data

Handles high-dimensional features

Robust to class imbalance using class weights

Captures non-linear relationships

3️⃣ LSTM Autoencoder (Unsupervised)

Trained only on normal behavior

Captures temporal dependencies in sensor data

Detects anomalies using reconstruction error

Threshold set using percentile-based strategy

4️⃣ Hybrid Fusion Strategy

Final anomaly decision is made by combining:

Random Forest prediction

LSTM-AE reconstruction error

This fusion improves recall and reduces false negatives.

🧪 Experimental Results
🔍 Model Performance Comparison
Model	Accuracy	Precision	Recall	F1-Score
Random Forest	92%	90%	88%	89%
LSTM Autoencoder	95%	93%	94%	93%
Hybrid Model	97%	96%	97%	96%
✔ Key Observations

Random Forest performs well on known attacks

LSTM Autoencoder detects unseen anomalies

Hybrid model achieves the best overall performance

High recall ensures minimal missed attacks

📂 Repository Structure
Hybrid-ML-Anomaly-Detection-SWaT/
│
├── notebook/
│   └── Hybrid_ML_Anomaly_Detection_SWaT.ipynb
│
├── report/
│   └── Hybrid_ML_Anomaly_Detection_SWaT.pdf
│
├── results/
│   ├── accuracy_plot.png
│   └── confusion_matrix.png
│
├── requirements.txt
└── README.md

▶️ How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/your-username/Hybrid-ML-Anomaly-Detection-SWaT.git
cd Hybrid-ML-Anomaly-Detection-SWaT

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Run the Notebook

Open notebook/Hybrid_ML_Anomaly_Detection_SWaT.ipynb

Run cells sequentially in Jupyter Notebook or Google Colab

⚙️ Requirements

The project uses the following libraries:

Python 3.8+

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn

TensorFlow / Keras

All dependencies are listed in requirements.txt.

📄 Project Report

A detailed academic report explaining:

Problem formulation

Literature review

Model design

Experimental results

Discussion and conclusion

📄 Report available in:
/report/Hybrid_ML_Anomaly_Detection_SWaT.pdf

🚀 Future Improvements

Real-time streaming anomaly detection

Explainable AI (SHAP / feature attribution)

Deployment on edge or PLC-integrated systems

Evaluation on additional CPS datasets

Transformer-based temporal models

👨‍💻 Author

Tahir Ahmad
Software Engineering Student
Domain: Artificial Intelligence & Cybersecurity

📜 License

This project is developed for educational, research, and internship purposes.
You are free to use and extend it with proper attribution.
