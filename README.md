# DataMining
#### Project: Airline case study. 
#### Question: Find out what causes the most delay to your flight and predict it.
#### Data: The data set is collected from the airlines of the United States(3593 lines).
#### Algorithms: Linear regression vs Lasso regression, KNN, Navie bayes, Descision tree.
#### Analysis
- Prepare dataset
- Load data
- Input: “Carrier”, “Airport_Distance”, “Number_of_flights”, “Weather”, “Support_Crew_Available”, “Baggage_loading_time”,“Late_Arrival_o”, “Cleaning_o”,“Fueling_o”, “Security_o” AND Output: “Arr_Delay”
- Check the correlation between variables
- Split the data into 70% train and 30% test  
- Build the model with all input variables and check which variables do not affect categorical variable
- Delete the unaffected variables and build the model with the affected variables
- Apply algorithms to the model
Note: When I use KNN, naive bayes, and Descision tree algorithms, I need to convert the output data to binary form."factor(ifelse(df1$Arr_Delay >80 ,1 ,0))". Here number is 80 because it is between Q1 and Q3(49<= number <= 90)
#### formula
##### Regression 
- <img src="https://latex.codecogs.com/svg.image?&space;Y_i=&space;\beta_0&space;&plus;&space;\beta_1x_{i1}&space;&plus;&space;\beta_2x_{i2}&space;&plus;&space;...&space;&plus;&space;\beta_px_{ip}&space;&plus;&space;\epsilon" title=" Y_i= \beta_0 + \beta_1x_{i1} + \beta_2x_{i2} + ... + \beta_px_{ip} + \epsilon" />
- (Lasso regression) Objective = RSS + α * (sum of absolute value of coefficients)  
- <img src="https://latex.codecogs.com/svg.image?RMSE&space;=&space;\sqrt{\frac{\displaystyle\sum_{i=1}^n(Y_i&space;-&space;\hat{Y_i})^2}{n}}" title="RMSE = \sqrt{\frac{\displaystyle\sum_{i=1}^n(Y_i - \hat{Y_i})^2}{n}}" />
- <img src="https://latex.codecogs.com/svg.image?R^2&space;=&space;Cor(Y_i&space;-&space;\hat{Y_i})^2" title="R^2 = Cor(Y_i - \hat{Y_i})^2" />
##### classification
- <img src="https://latex.codecogs.com/svg.image?Accuracy&space;=&space;\frac{TP&space;&plus;&space;TN}{TP&space;&plus;&space;TN&space;&plus;&space;FP&space;&plus;&space;FN}&space;" title="Accuracy = \frac{TP + TN}{TP + TN + FP + FN} " />
- <img src="https://latex.codecogs.com/svg.image?Pos_Pred_Value&space;&space;=&space;Recall&space;=&space;\frac{TP}{TP&space;&plus;&space;FN}&space;" title="Pos_Pred_Value = Recall = \frac{TP}{TP + FN} " />
- <img src="https://latex.codecogs.com/svg.image?Neg&space;Pred&space;Value&space;=&space;\frac{TN}{TN&space;&plus;&space;FP}" title="Neg Pred Value = \frac{TN}{TN + FP}" />
- <img src="https://latex.codecogs.com/svg.image?Sensitivity&space;=&space;Precision&space;=&space;\frac{TP}{TP&space;&plus;&space;FP}" title="Sensitivity = Precision = \frac{TP}{TP + FP}" />
- <img src="https://latex.codecogs.com/svg.image?Specificity&space;=&space;\frac{TN}{TN&space;&plus;&space;FN}&space;" title="Specificity = \frac{TN}{TN + FN} " />
- <img src="https://latex.codecogs.com/svg.image?Kappa&space;=&space;\frac{P_0&space;-&space;P_e}{1-P_e}" title="Kappa = \frac{P_0 - P_e}{1-P_e}" />
- <img src="https://latex.codecogs.com/svg.image?P_0&space;=&space;Accuracy&space;" title="P_0 = Accuracy " />
- <img src="https://latex.codecogs.com/svg.image?P_e&space;=&space;\displaystyle\sum_{i=1}^n(\frac{n_i}{N}*&space;\frac{m_i}{N})" title="P_e = \displaystyle\sum_{i=1}^n(\frac{n_i}{N}* \frac{m_i}{N})" />
#### Good luck

