# House Price Prediction using Linear Regression

## Project Overview
This project uses Linear Regression to predict house values based on housing-related features from the California Housing dataset. The goal is to understand the basic machine learning workflow, from exploring data to evaluating model performance.

## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Dataset
The California Housing dataset was loaded using `fetch_california_housing()` from Scikit-learn.

- Total records: 20,640
- Input features: 8
- Target variable: `MedHouseVal`
- Missing values: None

The target values are expressed in units of $100,000.

## Project Steps
1. Loaded and explored the dataset.
2. Checked data types and missing values.
3. Visualized the distribution of house values.
4. Examined the relationship between median income and house values.
5. Split the data into training and testing sets.
6. Trained a Linear Regression model.
7. Evaluated the model using MAE, RMSE, and R².
8. Visualized actual versus predicted values and model residuals.

## Model Results

| Metric | Result |
|---|---:|
| Mean Absolute Error (MAE) | 0.533 |
| Root Mean Squared Error (RMSE) | 0.746 |
| R² Score | 0.576 |

The model explains approximately 57.6% of the variation in house values on the test set. The results indicate that the model captures some patterns in the data, but prediction accuracy could be improved.

## Conclusion
This project provided practical experience with data exploration, visualization, Linear Regression, prediction, and model evaluation. It also highlighted the importance of examining prediction errors and understanding dataset limitations.
