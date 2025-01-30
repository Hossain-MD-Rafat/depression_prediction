# Machine Learning Model for Depression Prediction

## Overview
This project aims to predict depression levels based on various personal, academic, and professional attributes. It utilizes machine learning models such as Decision Trees, Random Forests, Support Vector Machines (SVM), and Stochastic Gradient Descent (SGD) classifiers to analyze a dataset containing information on individuals.

## Dataset
The dataset consists of two CSV files:
- `train.csv`: Used for training the models.
- `test.csv`: Used for model evaluation.

### Key Features
- Categorical attributes: Profession, Dietary Habits, Degree, etc.
- Numerical attributes: CGPA, Work Pressure, Financial Stress, Academic Pressure, etc.
- Target variable: `Depression`

## Data Preprocessing
### Handling Missing Values
- Mode imputation for categorical features (Profession, Dietary Habits)
- Median imputation for numerical features (CGPA, Work Pressure, Academic Pressure, Study Satisfaction, Job Satisfaction)
- Mean imputation for Financial Stress

### Duplicate Removal
- Identifies and removes duplicate entries from the dataset.

### Outlier Detection and Treatment
- Uses IQR (Interquartile Range) method to detect and cap outliers in numerical columns such as `Study Satisfaction`, `CGPA`, and `Academic Pressure`.

## Data Visualization
- Histograms for numerical features
- Correlation heatmap to understand feature relationships
- Pair plots to visualize feature distributions

## Feature Engineering
- Dropped columns: CGPA, Academic Pressure, and Study Satisfaction to remove redundant or highly correlated features.
- Encoded categorical variables using `OrdinalEncoder`.
- Standardized numerical features using `StandardScaler`.

## Model Training and Evaluation
### Machine Learning Models Used
- **Decision Tree Classifier**
- **Random Forest Classifier**
- **Support Vector Classifier (SVC)**
- **Stochastic Gradient Descent (SGD) Classifier**

### Model Training
- Data is split into 80% training and 20% testing.
- Models are trained and evaluated using accuracy, precision, recall, F1-score, and cross-validation.
- Overfitting analysis by comparing training and testing accuracy.

### Performance Evaluation
- Classification report and accuracy scores are generated for each model.
- Cross-validation is performed using Stratified K-Fold.
- Training times for each model are measured and compared.
