This code analyzes residential electricity consumption patterns using a UK smart meter dataset.  It employs several time series models for prediction and comparison.

**Key Features:**

1. **Data Loading and Preprocessing:** The script begins by loading the dataset (LCL-June2015v2_99.csv), handling data type conversions, and exploring the data through visualizations (time-series plots, distributions, and box plots).  It also cleans the data by removing unnecessary columns, handling missing values, and converting the energy consumption to numeric values.  Monthly averages of energy consumption are calculated and plotted.

2. **Feature Engineering:** The code engineers a new feature, energy\_kWh, representing energy consumption in kilowatt-hours, handles missing values and sets the DateTime column as the index, creating a time series dataset.

3. **Data Scaling:**  It normalizes the 'energy\_kWh' data using MinMaxScaler to improve model performance.

4. **Sequence Creation:**  The code transforms the time series data into sequences of a specified length (24 half-hour periods in this case) to prepare it for recurrent neural networks.

5. **Model Training and Evaluation:** Three different models are trained and evaluated:
    * **Recurrent Neural Network (RNN):** A simple RNN model is trained to predict future energy consumption based on past consumption patterns.  The performance is measured using Root Mean Squared Error (RMSE) and Accuracy.
    * **Long Short-Term Memory (LSTM) Network:**  An LSTM network is trained and evaluated similarly to the RNN, leveraging its ability to learn long-term dependencies in sequential data.  The performance is also measured using RMSE and Accuracy.
    * **Prophet:** The Facebook Prophet model, designed for time series forecasting, is also used. It predicts future consumption and measures RMSE and Accuracy.

6. **Result Visualization:** The code compares the performance of the three models using bar charts, visualizing both RMSE and accuracy. The components of the Prophet model are also visualized.

**Dependencies:**

The code relies on several Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow, prophet.  Make sure these libraries are installed before running the script.

**To run:**

1.  Make sure you have the `LCL-June2015v2_99.csv` file in the same directory as the script or provide the correct path to the file.
2.  Execute the Python code in an environment with the necessary libraries.


This script provides a comprehensive analysis of energy consumption patterns, showcasing the application and comparison of different forecasting models. The results offer insights into the predictive capabilities of each method.
