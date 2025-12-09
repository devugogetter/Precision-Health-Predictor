# Precision Health Predictor
Integrating **Clinical Biomarkers** and **Gene Expression** (Omics) for Early Mortality and **Sepsis Risk Prediction**

## Project Overview
This project was developed as part of **Biocodethon 2025**, where our team emerged as Winners 🏆.
The goal was to build a fast, interpretable, clinically meaningful ML pipeline that fuses both:
- Clinical health parameters (Heart Failure Clinical Dataset)
- Gene expression profiles (GEO – GSE54514 Sepsis Dataset)
to generate a hybrid prediction system for patient risk assessment.

The project demonstrates the power of **early disease prediction**, **multi-modal data fusion**, and **explainable AI** in next-gen precision medicine.

## Key Features

**1. Dual-Input Architecture**

- Logistic Regression on clinical biomarkers
- Random Forest on microarray gene-expression data
- Probability-level fusion → robust risk score

**2. Explainable AI (SHAP)**

- Global feature importance
- Patient-level “force plots” showing risk drivers
- Easy to communicate to clinicians & stakeholders

**3. Clean, Reproducible Pipeline**

- Fully runnable in a Jupyter Notebook
- Minimal dependencies
- Clear modular design (preprocessing → modeling → fusion → interpretation)

**4. Beautiful Visualizations**

- ROC curves for each model
- SHAP interpretation
- PCA projection
- Risk distribution
- Patient-level risk gauge (Plotly)

<img width="1086" height="350" alt="Mortality Risk Gauge" src="https://github.com/user-attachments/assets/cb89fc61-08c5-4a9c-8589-bb8a1958f897" />

## Datasets Used
1️. **Clinical Dataset**: Heart Failure Clinical Records

2️. **Gene-Expression Dataset**: GSE54514 (Sepsis Study)
- Source: NCBI GEO
- Microarray gene-expression data from septic vs. healthy subjects.

## Pipeline Architecture
            ┌─────────────────────┐
            │ Clinical Data (EHR) │
            └───────────┬─────────┘
                        │
          Logistic Regression Model
                        │
                        ▼
                  Clinical Risk
                        │
───────────────────────────────────────► Fusion Layer ► Final Risk Score
       
                        │
                  Omics Risk
                        ▲
          Random Forest Classifier
                        │
            ┌─────────────────────┐
            │  Gene Expression    │
            └─────────────────────┘
