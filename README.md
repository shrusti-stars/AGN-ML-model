# AGN-ML-model: Machine Learning Pipelines for AGN Excitation Mode Classification
This repository contains all code, data processing, and machine learning notebooks for the thesis project:
**“Machine Learning Classification of Radio-Loud AGN Excitation Modes (HERG/LERG) in Large Galaxy Surveys.”**

The project builds and applies machine learning pipelines to classify radio-loud AGN (RLAGN) based on host galaxy properties, using methods inspired by Janssen et al. (2012) and Best & Heckman (2012).

---

## Project Structure

- **BHML/**: Pipeline using features and labels from Best & Heckman (2012)
- **JanssenML/**: Pipeline following the feature logic of Janssen et al. (2012)
- **lotssML/**: Application of the trained ML model to the LoTSS DR2 AGN value-added catalogue
- **notebooks/**: Jupyter notebooks for data cleaning, feature engineering, and model training/testing
- **data/**: Scripts and instructions for sourcing external data (catalogs not included)

---

## Scientific Objective

- Classify RLAGN into High-Excitation (HERG) and Low-Excitation (LERG) modes
- Explore how host galaxy properties (mass, color, emission line ratios) influence AGN type
- Extend traditional excitation-mode analysis with modern ML approaches
- Validate results across SDSS (optical) and LOFAR LoTSS (radio) surveys

---

## Pipelines Included

- **BHML**: Baseline RLAGN classification using the Best & Heckman 2012 feature set
- **JanssenML**: Advanced classifier with Janssen et al. (2012)-inspired features (emission line ratios, color, stellar mass)
- **lotssML**: Cross-survey application and validation on the LoTSS DR2 catalogue

All pipelines use **Random Forest classifiers** and standard evaluation metrics (accuracy, precision, recall, F1-score, ROC AUC).

---

## How to Use

1. Download the required value-added galaxy/radio catalogs (see `data/` instructions)
2. Follow the workflow in each notebook for data preparation, training, and analysis

---
_______________



# RLAGN HERG/LERG Classification Pipeline (BHML)

This file contains a machine learning pipeline for classifying radio-loud AGN (RLAGN) into high- and low-excitation types (HERG/LERG), based on the approach and features from Best & Heckman (2012).

---

- **Data Sources**

- SDSS DR7 main galaxy sample  
- Best & Heckman (2012) RLAGN catalogue  
- MPA-JHU value-added galaxy properties

---

- **Pipeline Highlights**

- Data cleaning and merging for RLAGN samples
- Feature engineering using core host galaxy properties (e.g., stellar mass, color)
- Random Forest classifier for excitation mode (HERG vs. LERG)
- Implements the “BHML” feature set (Best & Heckman 2012)
- Provides baseline for comparison with more advanced models (e.g., JanssenML)

---

- **Purpose**

- Reproduce classical HERG/LERG separation based on the Best & Heckman scheme
- Serve as a baseline for evaluating feature extensions (e.g., emission-line diagnostics)
- Enable RLAGN classification in SDSS-based galaxy/radio samples

---

*This pipeline serves as the foundation for extended models (see JanssenML/), allowing direct comparison between classical and ML-based excitation mode separation.*

---


# RLAGN HERG/LERG Classification Pipeline (JanssenML)

This file contains a machine learning pipeline for classifying radio-loud AGN (RLAGN) into high- and low-excitation types (HERG/LERG), following Janssen et al. (2012).

- **Data sources:**  
  - SDSS DR7 main galaxy sample  
  - Best & Heckman (2012) / Janssen et al. (2012) RLAGN catalogs  
  - MPA-JHU value-added galaxy properties

- **Pipeline highlights:**  
  - Data preparation and feature engineering for RLAGN host galaxies  
  - Emission line diagnostics and host parameters (stellar mass, color, line ratios)  
  - Random Forest classifier for excitation mode (HERG vs. LERG)  
  - Implements and extends “Janssen ML” feature set (see paper)  
  - Easily adaptable for cross-survey applications (e.g., LoTSS DR2)

- **Purpose:**  
  - Reproduces and extends classical excitation-mode separation in RLAGN  
  - Enables robust selection of HERG/LERG candidates in large optical+radio datasets  

**See `janssen_huubML/` for step-by-step analysis, code, and figures.**

*This pipeline extends the previous “BHML” model and incorporates feature logic from Janssen et al. (2012).*

---
# RLAGN HERG/LERG ML Application to LOFAR LoTSS DR2 (lotssML)

This directory contains code for applying the SDSS-trained machine learning classifier (HERG/LERG, Random Forest) to the LOFAR LoTSS DR2 AGN value-added catalogue.

---

- **Data Sources**

- LOFAR LoTSS DR2 AGN catalogue (Hardcastle et al. 2023)
- Feature engineering based on columns available in both SDSS and LoTSS (e.g., stellar mass, rest-frame color, emission-line ratios)

---

- **Pipeline Highlights**

- Adapts the SDSS-trained RLAGN classifier to the LoTSS DR2 sample
- Harmonizes feature engineering for cross-survey compatibility
- Predicts HERG probabilities for LoTSS RLAGN
- Compares ML predictions to LoTSS catalogue HERG/LERG labels (where available)
- Analyzes HERG/LERG distribution as a function of host galaxy and radio properties in LoTSS

---

- **Purpose**

- Validate the generalizability of the ML classifier to new, deeper radio surveys
- Enable robust selection of HERG/LERG candidates in LoTSS for further astrophysical studies
- Provide direct cross-survey comparison between optical (SDSS) and radio (LoTSS) AGN populations

---

**See the main notebook for feature extraction, model inference, and result visualization.**

*This pipeline application and validation of RLAGN classifier in the next-generation LoTSS survey environment.*

---
 



