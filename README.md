# Predicting Wrongful Convictions

## Overview  
This project investigates whether the **intensity of wrongful convictions** in the U.S. justice system can be predicted using **demographic information** and **contributing factors**.  

The goal is to predict two outcomes for exonerees:  
- **Sentence length** (classification)  
- **Time spent in prison** (regression)  

**Inputs include:**  
- **Demographics**: State, Race, Sex  
- **Contributing Factors**:  
  - Official Misconduct  
  - False Forensic Analysis  
  - False Confessions  
  - False Accusations  
  - Mistaken Eyewitness Identification  
  - Inadequate Defense  

Data comes from the [National Registry of Exonerations](https://www.law.umich.edu/special/exoneration/Pages/about.aspx).

---

## Methods  
- **Data Cleaning & Engineering**  
  - Encoded categorical features into numeric/dummy variables  
  - Bucketized sentence lengths into 9 categories (e.g., “Life,” “More than 40 years,” “Less than 10 years”)  
  - Computed time spent in prison (log-transformed)  

- **Model**  
  - Built a **feed-forward neural network** in TensorFlow  
  - Dual outputs:  
    - **Regression** → Time Spent in Prison (log)  
    - **Classification** → Sentence Category Number  
  - **Hyperparameters:**  
    - 14 epochs, batch size 100, learning rate 0.01  
    - ReLU activations for hidden layers  
    - Linear activation (regression) / Softmax activation (classification)  

---

## Results  
- **Sentence Classification**: ~55% accuracy (vs. 22% random chance)  
- **Time in Prison (Regression)**: Mean Absolute Error ≈ 6.8 years  

While classification performed better than chance, regression results were unreliable. The model may offer a starting point for case prioritization but is not ready for real-world application.  

---

## Limitations  
- **Labeling Challenges**: Bucketizing sentences led to information loss  
- **Data Gaps**: Dataset excludes wrongful convictions not yet exonerated  
- **Practical Use**: Contributing factors may not always be known before trial  

