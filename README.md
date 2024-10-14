# Electricity-consumption
# 1. Data Loading and Preprocessing:
    - Loads the electricity consumption dataset from a CSV file.
    - Cleans the data by handling missing values and converting relevant columns to appropriate data types.
    - Extracts time features (hour, day, month, weekday) from the DateTime column.

# 2. Exploratory Data Analysis (EDA):
    - Performs basic EDA to understand the dataset, such as checking for missing values, examining data distributions, and visualizing energy consumption patterns.

# 3. Model Training and Evaluation:
    - Splits the dataset into training and testing sets.
    - Trains three regression models (Linear Regression, Decision Tree, Random Forest) to predict electricity consumption based on extracted time features.
    - Evaluates the models using Mean Absolute Error (MAE) and Mean Squared Error (MSE) to compare their performance on the test data.

# 4. Model Performance Visualization:
    - Creates bar plots to visualize the MAE and MSE for each model, facilitating a comparison of their prediction accuracy.

# 5. Summary:
    - The code demonstrates a typical machine learning workflow for predicting electricity consumption using regression models. 
    - It analyzes the relationship between time features and energy consumption patterns, helps understand electricity usage trends and provides a foundation for further analysis or optimization. 

