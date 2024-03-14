# data-modeling-real-estate

# Model Training:

We started by training several regression models using different algorithms: Linear Regression, Ridge Regression, Lasso Regression, and Random Forest Regression.
For each model, we set up a pipeline to preprocess the data. In this preprocessing step, we scaled the numerical features using StandardScaler to ensure that each feature has a mean of 0 and a standard deviation of 1, which helps improve the performance of some machine learning algorithms.
After setting up the pipelines, we trained each model using the training data.

# Model Evaluation:

Once the models were trained, we evaluated their performance using several metrics:
Mean Squared Error (MSE): This measures the average squared difference between the predicted values and the actual values. Lower values indicate better performance.
Root Mean Squared Error (RMSE): This is the square root of the MSE and provides a measure of the average magnitude of the errors. Lower values indicate better performance.
R-squared (R2) Score: This metric indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. Higher values (closer to 1) indicate better fit.
Explained Variance Score: This metric quantifies the proportion of variance in the dependent variable that is explained by the independent variables. Higher values indicate better fit.
We computed these metrics for each model based on their predictions on a validation set.

# Model Selection:

Based on the evaluation metrics, we selected the Random Forest Regression model as it achieved the best performance overall. It had the lowest MSE and RMSE and the highest R-squared and Explained Variance scores among all the models.

# Model Persistence:

After selecting the Random Forest Regression model, we saved it to disk using the joblib library. This step is important as it allows us to reuse the trained model later without having to retrain it every time.

# Model Loading and Prediction:

In this step, we loaded the saved Random Forest Regression model from the file.
We then defined new data points for prediction, representing features of new instances for which we wanted to predict unit prices.
Using the loaded model, we made predictions on these new data points to obtain the predicted unit prices.

# Summary:

Overall, the exercise involved training multiple regression models, evaluating their performance using various metrics, selecting the best-performing model, saving it for future use, loading the saved model, and finally using it to make predictions on new data points.
The Random Forest Regression model was chosen due to its superior performance in terms of prediction accuracy, as evidenced by lower MSE and RMSE, and higher R-squared and Explained Variance scores compared to other models.
