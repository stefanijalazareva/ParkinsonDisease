# ParkinsonDisease


This project, implemented as a Jupyter Notebook, focuses on analyzing voice data to potentially assist in the diagnosis and monitoring of Parkinson's disease. It involves data loading, preprocessing, and the application of machine learning models to classify individuals based on their voice characteristics.


Parkinson's Disease Voice Analysis
This project, implemented as a Jupyter Notebook (ParkinsonsAnalysis.ipynb), focuses on analyzing voice data to potentially assist in the diagnosis and monitoring of Parkinson's disease. It involves data loading, preprocessing, and the application of machine learning models to classify individuals based on their voice characteristics.


Table of Contents
 - Project Overview
 - Dataset
 - Methodology
 - Key Findings and Recommendations
 - Installation and Usage
 - Dependencies


The main objective of this project is to explore the use of voice measurements for Parkinson's disease analysis. The notebook performs an in-depth analysis of various voice parameters (e.g., jitter, shimmer, pitch disturbances) to identify patterns that differentiate healthy individuals from those with Parkinson's.


The analysis uses a dataset named parkinsons.data, which contains various voice features. The dataset includes 195 entries and 25 columns, with no missing values. A new column, 'patient', is created by extracting patient IDs from the 'name' column.

Key columns in the dataset include:

- MDVP:Fo(Hz): Average vocal fundamental frequency
- MDVP:Fhi(Hz): Maximum vocal fundamental frequency
- MDVP:Flo(Hz): Minimum vocal fundamental frequency
- MDVP:Jitter(%), MDVP:Jitter(Abs), MDVP:RAP, MDVP:PPQ, Jitter:DDP: Measures of variation in fundamental frequency
- MDVP:Shimmer, MDVP:Shimmer(dB), Shimmer:APQ3, Shimmer:APQ5, MDVP:APQ, Shimmer:DDA: Measures of variation in amplitude
- NHR, HNR: Noise-to-harmonics ratio and harmonics-to-noise ratio
- status: Health status (1 for Parkinson's, 0 for healthy)
- RPDE, DFA: Non-linear dynamical complexity measures
- spread1, spread2, D2, PPE: Various other non-linear measures
- patient: Unique identifier for each patient


Parkinson's Disease Voice Analysis

This project, implemented as a Jupyter Notebook (ParkinsonsAnalysis.ipynb), focuses on analyzing voice data to potentially assist in the diagnosis and monitoring of Parkinson's disease. It involves data loading, preprocessing, and the application of machine learning models to classify individuals based on their voice characteristics.

Table of Contents
Project Overview
Dataset
Methodology
Key Findings and Recommendations
Installation and Usage
Dependencies
Project Overview
The main objective of this project is to explore the use of voice measurements for Parkinson's disease analysis. The notebook performs an in-depth analysis of various voice parameters (e.g., jitter, shimmer, pitch disturbances) to identify patterns that differentiate healthy individuals from those with Parkinson's.

Dataset
The analysis uses a dataset named parkinsons.data, which contains various voice features. The dataset includes 195 entries and 25 columns, with no missing values. A new column, 'patient', is created by extracting patient IDs from the 'name' column.

Key columns in the dataset include:

MDVP:Fo(Hz): Average vocal fundamental frequency
MDVP:Fhi(Hz): Maximum vocal fundamental frequency
MDVP:Flo(Hz): Minimum vocal fundamental frequency
MDVP:Jitter(%), MDVP:Jitter(Abs), MDVP:RAP, MDVP:PPQ, Jitter:DDP: Measures of variation in fundamental frequency
MDVP:Shimmer, MDVP:Shimmer(dB), Shimmer:APQ3, Shimmer:APQ5, MDVP:APQ, Shimmer:DDA: Measures of variation in amplitude
NHR, HNR: Noise-to-harmonics ratio and harmonics-to-noise ratio
status: Health status (1 for Parkinson's, 0 for healthy)
RPDE, DFA: Non-linear dynamical complexity measures
spread1, spread2, D2, PPE: Various other non-linear measures
patient: Unique identifier for each patient



Methodology
- The notebook follows these general steps:
    - Data Loading: The parkinsons.data CSV file is loaded into a pandas DataFrame.
    - Feature Engineering: A 'patient' ID is extracted from the 'name' column.
    - Exploratory Data Analysis (EDA): Initial data inspection is performed using df.head(), df.info(), df.describe(), and df.isnull().sum() to understand data structure, types, descriptive statistics, and missing values.
    - Data Preprocessing: Data is scaled using StandardScaler.
    - Model Training: The notebook uses GroupKFold for cross-validation to ensure that samples from the same patient are not split across training and test sets. Logistic Regression and Random Forest Classifier models are employed.
    - Model Evaluation: Classification reports and accuracy scores are used to evaluate model performance.
 

Key Findings and Recommendations
The analysis provides several recommendations based on the voice data analysis:
- Early Detection Focus: Voice analysis offers potential for early detection of Parkinson's disease, especially for at-risk individuals.
- Regular Monitoring: Regular voice analysis can help monitor disease progression and treatment effectiveness.
- Intervention for Worsening: If patient-specific analysis shows signs of deterioration (status change or negative biomarker trends), therapeutic interventions like medication adjustments or physical/speech therapy should be considered.
- Focus on Key Attributes: Important identified attributes (e.g., MDVP:Fo(Hz), MDVP:Jitter(%), MDVP:Shimmer(%)) should be central to future research and diagnostic tool development.
- Decision Support System Development: Clinical decision support systems integrating voice analysis results can aid doctors in diagnosis and treatment planning.
