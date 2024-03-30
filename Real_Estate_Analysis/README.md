# Real Estate Analysis

## Background

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

This is Kaggle's competition: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview), and I rank top 35% on this project.

## Conclusion

In the analysis phase, we discovered that the majority of house sale prices are distributed between approximately $100,000 and $250,000. A heatmap was utilized to discern correlations between variables.

In the construction phase, seven distinct machine learning models were evaluated. Through the process of hyperparameter tuning, the best-performing model was identified.

To evaluate model performance, four metrics were employed: Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²). To recap, here are the rounded data for all seven models:


| Model | MAE      | MSE            | RMSE     | R²   |
|-------|----------|----------------|----------|------|
| GBM   | 14,313.61 | 499,237,819.99 | 22,343.63 | 0.93 |
| RF    | 16,161.57 | 704,789,628.22 | 26,547.87 | 0.90 |
| DC    | 24,720.72 | 1,681,732,362.96 | 41,008.93 | 0.76 |
| SVM   | 56,595.93 | 7,246,160,208.02 | 85,124.38 | -0.02 |
| KNN   | 24,444.92 | 1,906,615,323.18 | 43,664.81 | 0.73 |
| XGB   | 15,999.80 | 625,314,265.06 | 25,006.28 | 0.91 |
| LGBM  | 15,383.37 | 810,837,970.23 | 28,475.22 | 0.89 |

Upon review, the best model was determined to be the Gradient Boosting Machine (GBM), which outperformed all others across the evaluation metrics.

But there is a interesting thing: the score did't change a lot after hyperparameter tuning, it could show following reason:

If the scores didn't change after hyperparameter tuning, it could suggest a few different possibilities:

-  **Hyperparameter Range**: The ranges for hyperparameters chosen during tuning might not have been wide enough or appropriate to find a better solution than the default settings.

-  **Model Complexity**: The models may already be performing optimally with their default parameters, and the dataset may not benefit from more complex models or the hyperparameters you were tuning.
