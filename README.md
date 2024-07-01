# Introduction
This project is an assignment for the AI/ ML certification course offered by UC Berkeley. In this project, I am analyzing used car data set with different models to answer the question "What drives the price of a car"

**Jupyter Notebook with code, experimentation, further insights, and deployment strategies: [here](https://github.com/vivianamarquez/Regression-Sklearn-Diabetes-Dataset/blob/main/Regression_Example.ipynb).**

**Website for this repo: [here](https://vivianamarquez.com/Regression-Sklearn-Diabetes-Dataset/).**

## Business Goal

The goal is to understand what factors make a car more or less expensive. This will give clear recommendations to a used car dealership as to what consumers value in a car. The goal of this analysis is to develop predictive models that can forecast price of a used car based on various vehicle features. This can help car dealers to understand what are the important features in a car and increase sales.

## Data

The data set is used car data of 426K rows and 17 columns. The dataset contains 4 numeric variables, 13 categorical variables and the target variable is the price of a car.


![Distribution of Target Variable](images/histplot.png)

## Modeling and performance

In this project, we employed various regression modeling techniques to predict used car sale prices. The models evaluated include `Linear Regression`, `Ridge Regression`, `Lasso Regression`. Each model was trained and evaluated using a train/test split, followed by cross-validation and hyperparameter tuning using GridSearchCV to optimize performance. Due to the data set consisting of a large number of categorical variables, encoding them resulted in more than 11K columns, due to which training the set was a challenge. The cross validation, feature selection using SFS, hyperparameter tuning using GridSearchCV was not possible as the process ran for a long time.

Between Linear and Ridge Regression model, Ridge demonstrated the best performance with a `Root Mean Squared Error` (RMSE)  = 3832.3144, `R-squared` (R²) = 0.8751. That means that the model's prefictions are off by about 3832.3144 units from the actual values of price andapproximately 87.51% of the variance in the price as explained by the features in the model. 

The RMSE and R2 values indicate, the model can be improved significantly if we are able to figure out the important features and retrain the model.

<iframe src="https://vivianamarquez.com/Regression-Sklearn-Diabetes-Dataset/images/actual_vs_predicted.html" width="100%" height="600px"></iframe>

To see the interactive plot of actual vs. predicted values, please click the link below:
[Actual vs. Predicted Values](https://vivianamarquez.com/Regression-Sklearn-Diabetes-Dataset/images/actual_vs_predicted.png)


## Conclusions

The model revealed that there’s a significant relationship between certain features and the target variable (diabetes progression). Specifically, BMI, serum triglycerides, and blood pressure are positively associated with increased disease progression, while HDL cholesterol and T-Cells are negatively associated. These findings provide actionable insights for managing diabetes more effectively.

#### Interesting Findings

| Feature                                 | Recommendation                                                                                     | Coefficient Value | Impact               | Interpretation                                                                                  |
|-----------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|----------------------|-------------------------------------------------------------------------------------------------|
| Body Mass Index (BMI)                   | Implement and encourage weight management programs to reduce BMI.                                | 552.697775        | Strong positive      | Higher BMI is strongly associated with increased diabetes progression.                          |
| Serum Triglycerides (s5)                | Advocate for dietary changes that lower triglyceride levels, such as reducing sugar intake.       | 447.919525        | Strong positive      | Higher serum triglycerides levels are associated with increased diabetes progression.            |
| Blood Pressure (BP)                     | Encourage regular blood pressure monitoring and provide resources for managing high blood pressure. | 303.365158        | Significant positive | Higher blood pressure is associated with increased diabetes progression.                        |
| High-Density Lipoproteins (HDL) Cholesterol (s3) | Encourage diets rich in healthy fats to increase HDL levels.                                      | -229.255776       | Strong negative      | Higher HDL cholesterol levels are associated with decreased diabetes progression.                |
| Sex                                     | Develop personalized treatment plans that consider the patient’s sex.                            | -152.664779       | Significant negative | Differential impact based on sex, with higher values (likely males) associated with lower progression. |
| T-Cells (s1)                            | Focus on treatments and interventions that may boost T-Cells levels if applicable.                | -81.365007        | Moderate negative    | Higher levels of T-Cells are associated with decreased diabetes progression.                    |
| Blood Sugar Level (s6)                  | Provide education on managing blood sugar levels and ensure regular monitoring.                   | 29.642617         | Positive             | Higher blood sugar levels are associated with increased diabetes progression.                    |
| Age                                     | No specific recommendation needed based on this feature.                                          | 0.000000          | None                 | Age does not contribute to predicting diabetes progression.                                      |
| Low-Density Lipoproteins (LDL) Cholesterol (s2) | No specific recommendation needed based on this feature.                                          | 0.000000          | None                 | LDL cholesterol does not contribute to predicting diabetes progression.                          |
| Total Cholesterol/HDL Ratio (s4)        | No specific recommendation needed based on this feature.                                          | 0.000000          | None                 | The total cholesterol/HDL ratio does not contribute to predicting diabetes progression.          |


### Actionable insights

- **Weight Management Programs:** Develop and promote programs focused on weight management, such as nutrition counseling, exercise regimes, and support groups to help reduce BMI.

- **Blood Pressure Monitoring**: Encourage regular blood pressure check-ups and provide resources for managing high blood pressure through lifestyle changes and medication.

- **Personalized Care:** Develop personalized treatment plans that consider the patient’s sex to optimize care and manage diabetes progression more effectively.

- **Diet and Lifestyle Adjustments:** Encourage diets rich in healthy fats, such as those found in fish, nuts, and olive oil, to increase HDL cholesterol levels. Advocate for dietary changes that lower triglyceride levels, such as reducing sugar and refined carbohydrates intake.

- **Blood Sugar Control, Education and Tools:** Provide patients with education on managing blood sugar levels, including the use of glucometers and adherence to medication.
 
