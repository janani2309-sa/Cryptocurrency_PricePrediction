# Cryptocurrency Price Prediction

## Introduction
Cryptocurrencies are digital payment systems that operate on a peer-to-peer network, enabling secure and transparent transactions. With the growing importance of digital currencies, predicting their price movements can provide valuable insights for investors and analysts.

## Objectives
- To predict the pricing movements of cryptocurrencies, specifically Monero, Ethereum, Wrapped Bitcoin, and Bitcoin.
- To utilize a linear regression model for predicting future prices based on historical data.

## Dataset Used
The dataset used for this project includes historical price data for several cryptocurrencies. The columns in the dataset are:
- `SNo`: Serial Number
- `Name`: Name of the cryptocurrency
- `Symbol`: Symbol of the cryptocurrency
- `Date`: Date of the record
- `High`: Highest price of the day
- `Low`: Lowest price of the day
- `Open`: Opening price
- `Close`: Closing price
- `Volume`: Volume of the cryptocurrency traded
- `Marketcap`: Market capitalization

## Models/Techniques Used
### Linear Regression
Linear regression is a statistical method for modeling the relationship between a dependent variable and one or more independent variables. In this project, we used linear regression to predict future cryptocurrency prices based on historical data.

#### Steps Involved:
1. **Data Preprocessing**:
    - **Handling Missing Values**: Missing values in the dataset were handled by either removing the rows with missing values or filling them with appropriate values like mean or median.
    - **Removing Duplicates**: Duplicate records were removed to ensure data consistency.
    - **Data Normalization**: Features were scaled to a standard range to improve the performance of the regression model.

2. **Feature Engineering**:
    - **Target Variable**: A new target column was created to represent the future price of the cryptocurrency. For instance, if we aim to predict the price for the next day, the target variable will be the 'Close' price shifted by one day.
    - **Feature Selection**: Relevant features such as `Open`, `High`, `Low`, `Volume`, and `Marketcap` were selected as independent variables.

3. **Model Training**:
    - **Train-Test Split**: The dataset was split into training and testing sets. Typically, 80% of the data was used for training, and 20% was used for testing.
    - **Training the Model**: The linear regression model was trained using the training dataset. The model learns the relationship between the independent variables (features) and the dependent variable (target).

4. **Prediction**:
    - After training, the model was used to predict the future prices of cryptocurrencies on the testing dataset.

5. **Evaluation**:
    - **Mean Squared Error (MSE)**: MSE measures the average squared difference between the predicted and actual values. A lower MSE indicates a better fit.
    - **R-squared**: R-squared indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. A higher R-squared value indicates a better fit.

## Architecture
The linear regression model follows this architecture:
1. **Data Preprocessing**
    - Handling missing values
    - Removing duplicates
    - Data normalization
2. **Feature Engineering**
    - Creating target variable
    - Selecting relevant features
3. **Model Training**
    - Splitting data into training and testing sets
    - Training the linear regression model
4. **Prediction**
    - Predicting future prices using the trained model
5. **Evaluation**
    - Assessing model performance using MSE and R-squared metrics

## Methodology
1. **Data Collection**: Historical price data for cryptocurrencies.
2. **Data Cleaning**: Handling missing values, removing duplicates, and ensuring data consistency.
3. **Feature Engineering**: Creating a target variable for predicting future prices.
4. **Model Training**: Splitting the data into training and testing sets and training the linear regression model.
5. **Evaluation**: Assessing the model's performance using appropriate metrics.

## Results
The linear regression model provided predictions for future cryptocurrency prices. The performance of the model was evaluated using metrics such as Mean Squared Error (MSE) and R-squared.

## Discussion
The model demonstrated the ability to predict future prices with a reasonable level of accuracy. However, the volatile nature of cryptocurrency markets means that predictions can be uncertain. Future work could involve exploring more advanced models and incorporating additional features.

## How to Use This Project
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/cryptocurrency-prediction.git
    ```
2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Jupyter notebook:
    ```bash
    jupyter notebook cryptocurrency-prediction.ipynb
    ```

## Conclusion
This project showcases the use of linear regression models for predicting cryptocurrency prices. While the model provides valuable insights, it's important to consider the inherent volatility of the market. Further research and model improvements could enhance prediction accuracy.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
