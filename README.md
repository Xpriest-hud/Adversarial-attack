# Adversarial-attack

Robust & Explainable Network Intrusion Detection

## Project Overview
This repository contains the implementation of a deep learning-based Network Intrusion Detection System (NIDS). The objective of this research is to highlight the structural vulnerabilities of standard Artificial Neural Networks to adversarial manipulation, and to deploy a robust countermeasure framework.

The system utilizes a Multi-Layer Perceptron (MLP) architecture that is subjected to a targeted Fast Gradient Sign Method (FGSM) evasion attack. It successfully defends against this attack using Robust Adversarial Retraining and integrates SHAP (SHapley Additive exPlanations) to resolve the deep learning "black box" problem.

## Dataset Information
This project utilizes network telemetry from the **CIC-IDS-2018** dataset, focusing specifically on brute-force attack vectors. 

**Note:** Due to GitHub's strict file size limitations (100MB), the 1.6GB dataset is not hosted directly in this repository. To reproduce this environment, ensure you have your Kaggle API key configured and run the following command:
`!kaggle datasets download -d solarmainframe/ids-intrusion-csv`

## Empirical Results
The adversarial hardening framework successfully eliminated the vulnerability gap without degrading performance on clean organizational traffic.

* **Baseline Model Accuracy (Clean Traffic):** 99.99%
* **Baseline Vulnerability (Under FGSM Attack):** 66.52% (Security Degradation of 33.47%)
* **Hardened Model Recovery (Under FGSM Attack):** 100.00%
* **Hardened Model False Negatives:** 0 (Complete Attack Deflection)

## Technologies & Frameworks Used
* **Machine Learning Engine:** TensorFlow / Keras
* **Explainable AI (XAI):** SHAP
* **Data Processing:** Pandas, NumPy, Scikit-Learn
* **Visualization:** Matplotlib
