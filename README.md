# ParkinsonDisease


This project focuses on analyzing and visualizing Parkinson's disease data using various data science techniques. Principal Component Analysis (PCA) is used to reduce the dimensionality of the dataset and help visualize the separation between healthy individuals and those with Parkinson’s disease. The project also includes steps for preprocessing, feature selection, and potentially training machine learning models for classification.

📁 Project Structure
ParkinsonDiseaseAnalysis.ipynb — Jupyter notebook containing all the code for loading, analyzing, visualizing, and modeling the data.
parkinsons.data - Dataset

📊 Dataset
The dataset used in this project contains biomedical voice measurements from individuals, some with Parkinson’s disease and some healthy. Each instance represents one recording with features such as frequency, jitter, shimmer, and more.

Target column: status
0 = Healthy
1 = Parkinson's disease

✅ Objectives
Load and explore the dataset

Perform data preprocessing (handling missing values, normalization, etc.)

Visualize the data using PCA

Understand how well PCA can separate the two classes (healthy vs Parkinson)

Train machine learning models to classify the disease

Other dimensionality reduction techniques (t-SNE)

Implement classifiers (SVM, Random Forest, KNN)

Perform model evaluation (accuracy score)


📈 PCA Visualization
The PCA visualization reduces the dataset to two principal components, allowing us to see how the data points (patients) are distributed. The plot uses color to indicate disease status:

Red points indicate patients with Parkinson’s disease.

Blue points indicate healthy individuals.

🛠 Technologies Used
Python 3

NumPy, Pandas

Scikit-learn (for PCA and ML)

Matplotlib, Seaborn (for visualization)

Jupyter Notebook
