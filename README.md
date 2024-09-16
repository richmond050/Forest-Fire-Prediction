# Forest Fire Prediction Using Weather and Spatial Data

## Project Overview

This project is aimed at predicting forest fire burned areas using a dataset from the Montesinho Park in Portugal. The dataset includes various weather features, spatial coordinates, and fire indices (FFMC, DMC, DC, ISI) which are crucial to estimating the likelihood and extent of fire spread. The goal was to apply machine learning techniques to predict the burned area of the forest based on these input features.

### Objectives:
- Use weather and fire indices as input features to predict forest fire burned areas.
- Apply and evaluate different machine learning models to explore which model provides the best predictive accuracy.
- Experiment with data transformations and feature engineering techniques to improve model performance.

---

## Dataset Description

The dataset used in this project contains the following variables:
- **Spatial Coordinates:** X and Y, representing the location within the park.
- **Weather Features:** Temperature (°C), wind speed (km/h), relative humidity (%), and rainfall (mm/m²).
- **Fire Weather Indices:** 
  - **FFMC (Fine Fuel Moisture Code):** Represents the moisture content of litter and fine fuels in a forest.
  - **DMC (Duff Moisture Code):** Represents the moisture content of loosely compacted organic matter.
  - **DC (Drought Code):** Represents the dryness of deeper, compact organic matter.
  - **ISI (Initial Spread Index):** Represents the potential for fire spread based on wind and moisture conditions.
- **Target Variable (Burned Area):** The area of forest burned (in hectares), which is highly skewed toward smaller values.

---

## Machine Learning Models Used

Three machine learning models were tested for predicting the forest fire burned area:

1. **Linear Regression**
   - **Mean Squared Error (MSE):** 1.797
   - **R² Score:** -0.050 (indicating the model struggles to capture meaningful relationships).

2. **Random Forest Regressor**
   - **Mean Squared Error (MSE):** 1.887
   - **R² Score:** -0.103 (slight improvement from linear regression, but still underperforming).

3. **Gradient Boosting Regressor**
   - **Mean Squared Error (MSE):** 1.941
   - **R² Score:** -0.134 (similar performance to the Random Forest model).

Although the models were tuned and log transformations were applied to the target variable, the models didn’t achieve positive R² values, indicating the predictions were weaker than expected. This highlights the challenges of predicting forest fire areas, especially with highly skewed data.

---

## Key Challenges and Observations

- **Data Imbalance:** The burned area variable is heavily skewed toward 0, making it difficult for the models to learn meaningful patterns.
- **Non-linear Relationships:** The relationships between the weather features, fire indices, and burned areas are complex, and the linear models struggled to capture them.
- **Overfitting Risk:** More complex models like Random Forest and Gradient Boosting may have overfit the training data, leading to suboptimal generalization on the test data.

---

## Future Work

This project provided valuable insights, but there’s still much to be improved. Going forward, I plan to:

- **Implement Advanced Models:** I'll explore models like **XGBoost** or **LightGBM**, which are known to perform better on structured datasets.
- **Feature Engineering:** I will create new features that capture interactions between variables, such as wind speed and temperature or relative humidity and fire indices.
- **Address Data Imbalance:** Techniques like **oversampling**, **undersampling**, or **smarter weighting** within the models will be applied to deal with the imbalance of the target variable.
- **Model Tuning and Cross-Validation:** I will further tune the models using more advanced hyperparameter optimization techniques.

I am still in the process of learning and improving my machine learning skills, and this project represents my first steps in applying these techniques to a real-world problem. The current models are far from perfect, but they form a foundation for future improvements.

---

## Conclusion

Predicting forest fire burned areas is a challenging task, especially given the complexity of the relationships between the input features and the target variable. While the initial models did not achieve high accuracy, they provide a starting point for further refinement. I plan to continue improving this model and applying more advanced techniques as I progress in my machine learning journey.

---

## Acknowledgements

This project uses data from the Montesinho Park, Portugal, and is inspired by previous work in fire weather indices.

---


