This repository contains the code for implementing and evaluating a Support Vector Machine (SVM) model to predict ADHD in individuals with Autism Spectrum Disorder (ASD). The code leverages an SRS scores dataset derived from ABIDE to train and test the SVM model and includes performance evaluation and feature importance analysis.<br>

python requirements:
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- joblib
- scipy


<br> 
The dataset used in this project is expected to be in the following directory structure: ../input/srsno-avg2/
The specific file required is MLsheet - SRSno-avg.csv. The dataset is a preprocessed version of the combined ABIDE I and II datasets, cleaned to include the SRS values and binary categorization of HAS_ADHD (0=ASD-only, 1=ASD+ADHD).


  
overview:  
1. Data: Loads the dataset, filters relevant columns, and splits it into training and testing sets.
2. Model training: Trains an SVM model with hyperparameter optimization using RandomizedSearchCV.
3. Model evaluation:
  - Prints the best parameters found and model accuracy.
  - Displays a classification report and confusion matrix.
  - Plots the calibration curve and scatter plots of SRS scores.
  - Generates and displays a correlation matrix.
4. Feature importance: Computes and plots permutation importance of features.
5. Model saving: Saves the trained model using joblib.
Access the SRS dataset here: https://www.kaggle.com/datasets/alainashinde/srsno-avg2/data 
  
note: The SRS-subscore correlation matrix is also computed and plotted within the code, but it is not included in the research paper. This is because the correlation matrix is typically used for reducing multicollinearity in linear regression models and isn't as relevant for the SVM (non-linear model) compared to permution feature importance as analyzed in the paper. It is provided here for additional examination and analysis.
