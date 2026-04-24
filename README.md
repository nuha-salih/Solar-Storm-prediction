# Solar-Storm-prediction
Machine learning model for predicting solar storms
# Solar Storm Impact on Communication Systems

### Machine Learning Prediction Project
**Najran University – Computer Science Department |  

## Project Overview

Solar storms can cause geomagnetic disturbances that disrupt satellites, GPS systems, and global communication infrastructure.

This project develops a machine learning-based system to predict solar storm events using solar wind data, providing an early warning mechanism to reduce potential risks.



## Problem Statement

Solar storms pose a significant threat to modern communication systems.
Existing approaches may fail to detect storms early enough, which increases the risk of service disruption and infrastructure damage.



## Research Question

Can machine learning models accurately predict solar storm events using solar wind data while prioritizing early detection over false alarms?



## Proposed Solution

This project implements a complete machine learning pipeline that analyzes solar wind measurements to predict geomagnetic storms.

A **safety-first strategy** is applied by using a custom decision threshold (0.3), where:

* Missing a storm (False Negative) is minimized
* Early detection is prioritized over strict accuracy

The system is designed to provide reliable early warnings for communication system protection.



## Dataset

* **Source:** NASA & NOAA
* **Platform:** Kaggle
* **Link:** https://www.kaggle.com/datasets/arashnic/soalr-wind
* **Type:** Numerical (Tabular)
* **Size:** 7,571,081 rows × 17 columns



## Features

* **Magnetic Field Components (GSE & GSM):**
  bx_gse, by_gse, bz_gse, bx_gsm, by_gsm, bz_gsm

* **Other Key Indicators:**

  * bt (Total magnetic field strength)
  * density (Particle density)
  * speed (Solar wind velocity)
  * temperature (Proton temperature)



## Target Variable

* **0 → No Storm** (dst > -50 nT)
* **1 → Storm Detected** (dst ≤ -50 nT)



## Models and Results

The following machine learning models were evaluated:

* Random Forest → 97.46% (Best Performance)
* K-Nearest Neighbors (KNN) → 97.26%
* Logistic Regression → 97.05%
* Decision Tree → 95.57%
* Naive Bayes → 93.11%

The Random Forest model achieved the best balance between accuracy and storm detection.



## Safety-First Optimization

A custom decision threshold of **0.3** was used to improve storm detection.

This approach increased the **Recall** score, allowing the model to detect approximately **99% of storm events**, which is critical in real-world applications.



## Visualization

To better understand model behavior, **Principal Component Analysis (PCA)** was used to reduce the dataset to two dimensions for visualization.

* Red regions represent predicted storm events
* Blue regions represent normal conditions
* Data points represent actual observations

This helps illustrate how models separate storm and non-storm cases.



## Technical Pipeline

1. Data collection and merging (~7.5 million records)
2. Data cleaning and preprocessing
3. Feature scaling
4. Model training and evaluation
5. Threshold optimization
6. Visualization using PCA and decision boundaries



## Requirements

```bash
pip install pandas scikit-learn matplotlib seaborn


```

## Future Work

* Integration with real-time solar data
* Deployment as an early warning system
* Enhanced feature engineering for improved accuracy

---

## Team Members


* Nuha Saleh Mohammed
*  Meznah Hadi Alrizq

---

## Supervisor

Dr. Hanan Halawani

---



