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
