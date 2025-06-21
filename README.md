# AGN-ML-model: Machine Learning Pipelines for AGN Excitation Mode Classification


This project applies machine learning models to predict AGN occurrences based on host galaxy properties, as an extension of the analysis presented in Janssen et al. (2012): "The Triggering Probability of Radio-Loud AGN: A Comparison of High and Low Excitation Radio Galaxies in Hosts of Different Colors".  

### Objective:
The machine learning model classifies AGNs into two categories based on their excitation types: High-Excitation Radio Galaxies (HERGs) and Low-Excitation Radio Galaxies (LERGs). The goal is to understand how different AGN types are influenced by host galaxy properties and their environments.


ML model is designed to classify AGNs based on their excitation (high-excitation vs. low-excitation) and link this to host galaxy properties. This would help to understand how different AGN types affect their host galaxies and environments differently.  
Model Type: A classification model (Random Forest).  
Features: may use host galaxy features (like color, mass, etc,.) and AGN features (radio luminosity, optical emission lines, etc.) as inputs to predict the AGN type.

Evaluation Metrics:  
For classification model (HERG vs. LERG classification): we use metrics like accuracy, precision, recall, F1-score, and ROC AUC to assess the model’s performance.

Once we have trained our ML model, we can analyze:
How AGN characteristics (radio luminosity, emission lines, etc.) relate to feedback mechanisms.






# RLAGN HERG/LERG Classification Pipeline (JanssenML)

This repository contains a machine learning pipeline for classifying radio-loud AGN (RLAGN) into high- and low-excitation types (HERG/LERG), inspired by Janssen et al. (2012).

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
  - Core code for thesis chapter and cross-survey validation

**See `janssen_huubML/` for step-by-step analysis, code, and figures.**

*This pipeline extends the previous “BHML” model and incorporates feature logic from Janssen et al. (2012).*

---
 



