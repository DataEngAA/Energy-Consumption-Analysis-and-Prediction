# Energy-Consumption-Analysis-and-Prediction

## Project Overview
This project aims to predict energy consumption in smart homes using a dataset containing various factors such as temperature, humidity, HVAC usage, occupancy, and other appliance usage. The goal is to build a machine learning model that can help forecast energy consumption based on these features and provide insights into which factors contribute most to energy usage.

## Dataset
The dataset used contains the following columns:

- `Date`: The date of energy usage
- `Home_ID`: Identifier for the home
- `City`: The city where the home is located
- `Energy_Consumption_kWh`: Energy consumption in kilowatt-hours (kWh)
- `Occupancy`: Binary value (0 or 1) indicating whether the home is occupied
- `Temperature_C`: Temperature in Celsius
- `Humidity_%`: Humidity level as a percentage
- `HVAC_Usage_kWh`: HVAC (Heating, Ventilation, Air Conditioning) usage in kilowatt-hours
- `Kitchen_Usage_kWh`: Energy consumption from kitchen appliances in kilowatt-hours
- `Electronics_Usage_kWh`: Energy consumption from electronic devices in kilowatt-hours

## Project Structure

### 1. Data Preprocessing
- Data was cleaned by handling missing values and addressing outliers.
- Features were normalized, and the dataset was split into training and test sets.
  
### 2. Model Training
- A linear regression model was trained to predict energy consumption (`Energy_Consumption_kWh`) based on the features.
  
### 3. Model Evaluation
- The model was evaluated using:
  - **Mean Absolute Error (MAE)**: 1.30
  - **R-squared**: -0.869
- Residual analysis was performed to check for any patterns or biases.
  
### 4. Feature Importance and Interpretation
- Key features affecting energy consumption were identified:
  - **Occupancy**: Coefficient of 0.630, indicating a significant positive effect on energy consumption.
  - **Temperature_C**: Coefficient of 0.322, contributing positively to energy consumption.
  - **HVAC_Usage_kWh**: Coefficient of -1.605, showing a negative relationship with total energy consumption, suggesting more complex dynamics.

### 5. Predictive System and Testing
- The trained model was used to predict energy consumption on the test data. The predicted values were compared with actual values using scatter plots and residual plots.

### 6. Results Summary
- Example of predictions:
Actual  Predicted
1.53   2.072061
3.74   5.806615

  
## Key Findings
- **Occupancy** and **Temperature** were the most influential factors in predicting energy consumption.
- The model's performance was suboptimal (R-squared: -0.869), suggesting that more advanced algorithms (e.g., decision trees, random forests) could improve the accuracy.

## Challenges
- Handling outliers and missing values required careful imputation strategies.
- The negative coefficient for HVAC usage indicated the need for further exploration of the relationship between HVAC and total energy consumption.

## Future Improvements
- Implement more complex machine learning models such as decision trees or ensemble methods to improve prediction accuracy.
- Perform more feature engineering to extract deeper insights from the dataset.

## Conclusion
This project highlights the potential of using linear regression to predict energy consumption in smart homes, although the model's accuracy suggests that more advanced models could yield better results. Feature importance analysis provides valuable insights into the factors driving energy usage, which can be leveraged to improve energy efficiency in smart homes.


  ```
 Run the Jupyter Notebook to view the full analysis or use the provided scripts to test the model.

## Dependencies
- Python 3.7+
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Author
Ali Ahmad
