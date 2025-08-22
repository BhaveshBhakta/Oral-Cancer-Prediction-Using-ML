## Oral Cancer Prediction Using ML

### Project Overview

This project aims to predict the **diagnosis of oral cancer** based on a comprehensive dataset of patient risk factors and clinical symptoms. By leveraging features such as age, gender, tobacco/alcohol use, HPV infection, and presence of oral lesions, the goal is to develop a machine learning model that can accurately classify whether a patient has oral cancer. This can assist in early detection and improved patient outcomes.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Oral Cancer Prediction Dataset](https://www.kaggle.com/datasets/ankushpanday2/oral-cancer-prediction-dataset)
  * **Size**: 84922 entries, 25 columns
  * **Key Features**:
      * `Age`, `Gender`, `Tobacco Use`, `Alcohol Consumption`, `Oral Lesions`, `Unexplained Bleeding`, and other lifestyle and clinical indicators.
  * **Approach**:
      * **Data Cleaning**: Dropped `ID` as it is a unique identifier. No missing values or duplicates were found.
      * **Exploratory Data Analysis**: Histograms, boxplots, and count plots were used for visualization to understand data distributions and class balance. The target variable is well-balanced.
      * **Label Encoding**: Applied to all categorical features. Numerical features were standardized using `StandardScaler`.
      * **Binary Classification**: The target variable `Oral Cancer (Diagnosis)` indicates a diagnosis of oral cancer ('Yes') or not ('No').
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **100%** with Logistic Regression, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, and SVC.
      * **99.8%** with Ridge Classifier.
      * The extremely high accuracies for most models suggest a very strong relationship between the features and the target, possibly indicating a data leakage issue.

-----

### Purpose and Applications

  * Assist medical practitioners in the **early screening and diagnosis of oral cancer**.
  * Identify individuals at high risk for oral cancer to facilitate preventive care and lifestyle changes.
  * Support public health initiatives by enabling a better understanding of oral cancer risk factors.
  * Serve as a tool for educational purposes in oncology and medical data analysis.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Oral-Cancer-Prediction-Using-ML.git
cd Oral-Cancer-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * **Investigating the very high accuracy for potential data leakage**. Features like `Tumor Size`, `Cancer Stage`, or `Survival Rate` are likely direct indicators of the diagnosis and should be excluded for a truly predictive model.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models to ensure robustness.
  * Exploring the impact of different feature selection or transformation techniques.
  * Adding explainability (e.g., SHAP or LIME) to understand which medical and lifestyle factors are most critical for oral cancer prediction.
