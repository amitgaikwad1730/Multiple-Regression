# Multiple-Linear-Regression

Multiple regression is an extension of simple linear regression. It is used when we want to predict the value of a variable based on the value of two or more other variables. The variable we want to predict is called the dependent variable (or sometimes, the outcome, target or criterion variable). The variables we are using to predict the value of the dependent variable are called the independent variables (or sometimes, the predictor, explanatory or regressor variables).

A very simple python program to implement Multiple Linear Regression using the LinearRegression class from sklearn.linear_model library.

The program also does Backward Elimination to determine the best independent variables to fit into the regressor object of the LinearRegression class.

The program uses the statsmodels.formula.api library to get the P values of the independent variables. The variables with P values greater than the significant value ( which was set to 0.05 ) are removed. The process is continued till variables with the lowest P values are selected are fitted into the regressor ( the new dataset of independent variables are called X_Optimal ).

X_Optimal is again split into training set and test set using the test_train_split function from sklearn.model_selection.

The regressor is fitted with the X_Optimal_Train and Y_Train variables and the prediction for Y_Test ( the dependent varibale) is done using the regressor.predict(X_Optimal_Test)
