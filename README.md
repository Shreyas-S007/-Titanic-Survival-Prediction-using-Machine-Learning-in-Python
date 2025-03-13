# 🚢 Titanic Survival Prediction

Predicting passenger survival on the Titanic using various machine learning models, enhanced with explainable AI techniques like LIME and SHAP.

## 📁 Project Structure

- `data/`: Contains the Titanic dataset.
- `notebooks/`: Jupyter notebooks detailing data exploration, preprocessing, modeling, and interpretability analyses.
- `models/`: Serialized trained models.
- `reports/`: Generated analysis reports and visualizations.
- `README.md`: Overview of the project.

## 📊 Dataset

The dataset includes features such as:

- `PassengerId`: Unique ID for each passenger.
- `Survived`: Survival indicator (0 = No, 1 = Yes).
- `Pclass`: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd).
- `Name`: Name of the passenger.
- `Sex`: Gender of the passenger.
- `Age`: Age of the passenger.
- `SibSp`: Number of siblings/spouses aboard.
- `Parch`: Number of parents/children aboard.
- `Ticket`: Ticket number.
- `Fare`: Fare paid.
- `Cabin`: Cabin number.
- `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

## 🛠️ Data Preprocessing

- **Handling Missing Values**: Imputed missing values in `Age`, `Embarked`, and `Cabin` features.
- **Encoding Categorical Variables**: Converted categorical variables like `Sex` and `Embarked` into numerical representations.
- **Feature Engineering**: Created new features such as `FamilySize` and `Title` extracted from passenger names.

## 📈 Exploratory Data Analysis (EDA)

Visualized relationships between features and survival rates:

- **Gender**: Higher survival rate for females.
- **Passenger Class**: 1st class passengers had higher survival rates.
- **Age**: Younger passengers had higher chances of survival.

*Example Visualization:*

![Survival Rate by Gender](reports/survival_rate_by_gender.png)

## 🤖 Modeling

Implemented and evaluated multiple models:

- **Logistic Regression**: Accuracy = 0.7989
- **Random Forest**: Accuracy = 0.8212
- **Support Vector Machine (SVM)**: Accuracy = 0.6536
- **Gradient Boosting**: Accuracy = 0.8156


## 🧠 Explainable AI

Employed LIME and SHAP to interpret model predictions:

- **LIME (Local Interpretable Model-Agnostic Explanations)**: Provided local explanations for individual predictions, highlighting the impact of each feature.

  *LIME Explanation Example:*

  ![LIME Explanation](reports/lime_explanation.png)

- **SHAP (SHapley Additive exPlanations)**: Offered global and local interpretability by assigning Shapley values to features, indicating their contribution to predictions.

  *SHAP Summary Plot:*

  ![SHAP Summary Plot](reports/shap_summary.png)

## 📝 Conclusion

- **Best Model**: Random Forest achieved the highest accuracy.
- **Key Features**: `Sex`, `Pclass`, and `Age` were the most influential features in predicting survival.
- **Interpretability**: LIME and SHAP provided valuable insights into model decision-making processes.

