# Industrial Defect Detection in Laser Cladding Process

## Overview
This repository presents a feasibility study of machine learning methods for early defect detection in an industrial laser cladding process used in engine head valve seat manufacturing.

The primary objective of the project was to evaluate and compare different ML approaches for classifying time-series data derived from process measurements, with a focus on early detection of rare defects.

---

## Business Context
Early identification of defects in manufacturing processes is critical to:
- reduce production costs,
- minimize scrap and rework,
- prevent costly downstream failures,
- improve overall process reliability.

This study investigates whether machine learning models can support these goals under real industrial data constraints.

---

## Process Description
The analyzed process is laser cladding of valve seats, including:
- identification of key process parameters,
- characterization of potential defect types,
- analysis of available sensor signals recorded during production.

---

## Data Challenges
The project addressed several real-world industrial data issues:
- highly imbalanced dataset with a very small number of defective samples,
- noisy time-series sensor data,
- limited number of recorded process parameters,
- constraints on data volume and labeling.

---

## Methodology

### Data Pipeline
- Data acquisition from industrial process sources
- Manual and semi-automated data labeling
- Data cleaning and preprocessing
- Feature engineering for time-series data

### Machine Learning Models
The following model architectures were implemented and evaluated:
- XGBoost (reference model)
- 1D Convolutional Neural Network (CNN)
- Recurrent Neural Networks:
  - LSTM
  - GRU

### Model Optimization
- Hyperparameter tuning using:
  - Optuna
  - GridSearchCV
- Evaluation using metrics suitable for imbalanced classification:
  - Recall
  - F2-score

---

## Results
- The GRU-based model achieved the highest performance in defect detection among the evaluated approaches.
- Overall model effectiveness was limited by data quality and class imbalance rather than model architecture.
- Deep learning models did not provide a decisive advantage without improvements in data collection strategy.

---

## Visualization
To support practical use and result interpretation, a dedicated visualization interface was implemented in the Ignition environment:
- real-time visualization of process parameters,
- display of classification results,
- support for operational monitoring by production staff.

---

## Key Findings
- Data quality and class imbalance are the dominant factors in industrial ML success.
- Model complexity alone cannot compensate for insufficient or noisy data.
- Early feasibility studies are essential before deploying ML systems in production environments.

---

## Conclusions and Future Work
The study demonstrates that ML-based defect detection in industrial environments requires:
- improved data acquisition strategies,
- increased number of defective samples,
- richer process parameterization.

Future improvements may include enhanced sensor coverage, better labeling processes and hybrid approaches combining domain knowledge with data-driven models.

---

## Tech Stack
- Python
- NumPy / Pandas
- scikit-learn
- XGBoost
- TensorFlow / PyTorch
- Optuna
- Ignition (industrial visualization)

---

## Project Status
🚧 Work in progress  
This repository is a recreated demo based on a university thesis.  
Code and experiments will be added incrementally.

---

## Disclaimer
This project is a recreated demonstration based on an academic thesis.  
No proprietary company data, code or confidential information is included.
