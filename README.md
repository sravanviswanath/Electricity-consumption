# Electricity-consumption
This code analyzes residential electricity consumption patterns using a dataset
likely from smart meters in the UK.

1. Data Loading and Preprocessing:
   - Loads a CSV file named 'LCL-June2015v2_99.csv'.
   - Converts the 'DateTime' column to a datetime format.
   - Extracts 'hour' and 'day' features from the 'DateTime' column.
   - Drops the original 'DateTime' and 'LCLid' columns.
   - Removes rows with missing values in 'KWH/hh (per half hour)' column.

2. Exploratory Data Analysis (EDA):
   - Displays basic information about the dataset like head, columns, info, and describe.
   - Checks for missing values in the dataset.
   - Visualizes the distribution of the 'KWH/hh (per half hour)' variable.

3. Feature Engineering:
   - Creates a new 'DayType' column representing the day of the week.

4. Data Visualization:
   - Creates a box plot showing energy consumption by day type.
   - Generates a histogram showing the distribution of energy consumption.

5. Modeling Preparation (Partially Implemented):
   - Selects 'stdorToU' as the independent variable (X) and 'KWH/hh (per half hour)' 
     as the target variable (y).
6. Data Modeling:
This section focuses on building and evaluating machine learning models to predict the
energy consumption ('KWH/hh (per half hour)') based on the available features.

1. Feature and Target Definition:
   - X: Represents the features used for prediction, specifically 'stdorToU'.
   - y: Represents the target variable, the energy consumption 'KWH/hh (per half hour)'.

2. Encoding Categorical Variables:
   - The 'stdorToU' column is treated as a categorical variable and is encoded
     using one-hot encoding. This transforms it into multiple binary columns,
     one for each unique value in 'stdorToU', where 1 represents the presence
     of that category and 0 represents absence.

3. Train-Test Split:
   - The dataset is split into training and testing sets using train_test_split.
     This enables us to train the models on a portion of the data and evaluate
     their performance on unseen data.

4. Model Selection:
   - Two machine learning models are employed: Random Forest Classifier and
     Decision Tree Classifier.

5. Model Training and Evaluation:
   - Each model is trained using the training dataset (X_train, y_train).
   - After training, the models make predictions on the test data (X_test), and
     the performance is assessed using the accuracy score and classification
     report. These metrics provide insights into the models' accuracy in
     classifying energy consumption patterns.

6. Visualization:
   - Scatter plots are generated to compare the actual energy consumption values
     against the predicted values for both models. These plots aid in
     understanding the model's performance visually and identifying any
     patterns in the deviations between actual and predicted values.


