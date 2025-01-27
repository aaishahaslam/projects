# projects

Retail sales project:
- objective: which time series model predicts retail sales in Queensland, Australia the best? Time series model needs to capture as much trend and seasonality as possible. Based on the ACF plots there is significant trend and temporal structure, so a model is needed to capture this underlying trend and structure and reduce the ACF as close to possible to white noise. From there, if we have a model that captures most of the temporal structure, we can use this model for predictons and assess how well the model is predicting the data through creating training/test datasets and using cross validation between different models. We compare RMSE's to assess model performance.
- Iterated through 53,000 model evaluations for forecasting to obtain performance metrics for 5 models across 10,600 training sets. Devised time series models that predict retail sale trends and seasonality in Queensland


Boston housing pricing project:
- objective: which predictors are best in predicting housing prices in Boston? how many predictors are necessary to get the best predictive model? We start with 13 variables (in pdf) that potentially explain variations in housing prices. First, we use a model with all 13 variables. Second, we make correlation matrices and train a random forest model to try to predict housing prices. From there we pick a potential second model based on the results. Then we fit a stepwise regression model for our third potential model which automatically choses a model based on lowest AIC values. Then we compare the performance of the 3 models using KNN algorithm which predicts validation sets and measures how accuretly it was predicted. 
- Achieved 78% predictive power for model using random forest, stepwise regression, and KNN algorithms to analyze variability in Boston housing prices


(see results ad additional details in pdf files, code is in qmd files)
