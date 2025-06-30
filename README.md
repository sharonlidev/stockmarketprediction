# Stock Market Prediction with Machine Learning

## 🚀 Project Purpose

The goal of this project is to build a simple but practical model that:

- Predicts whether the **S&P 500 Index** will rise or fall the next day
- Uses **logistic regression** as a baseline machine learning approach
- Illustrates key steps in data science workflows:
  - Data acquisition
  - Feature engineering
  - Model training
  - Model evaluation

This is **not financial advice** and is intended purely for educational purposes.

---

## 📈 How the Code Works

Here’s the high-level logic of the project:

1. **Load Historical Data**
    - Downloads historical daily prices for the S&P 500 from Yahoo Finance
    - Computes percentage daily returns

2. **Create Target Variable**
    - Labels each day as:
      - `1` → Market went up the next day
      - `0` → Market went down the next day

3. **Feature Engineering**
    - Calculates lagged returns:
      - Previous day’s return
      - Returns over previous 2-7 days
    - These lagged returns become model features

4. **Train/Test Split**
    - Splits the data into:
      - Training set (e.g. 70%)
      - Test set (30%)

5. **Model Training**
    - Uses **Logistic Regression** to predict the binary up/down outcome
    - Fits the model to the training data

6. **Model Evaluation**
    - Predicts on test data
    - Calculates:
        - Accuracy
        - Confusion matrix
        - Precision/Recall
    - Prints model coefficients to interpret feature importance

7. **Visualization (Optional)**
    - Plots predicted probabilities vs. actual outcomes

---

## 🛠️ Libraries Used

This project relies on:

- **Python 3.8+**
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [yfinance](https://pypi.org/project/yfinance/)
- matplotlib (optional for plots)

---

## 🤖 Machine Learning Model

- **Algorithm:** Logistic Regression
- **Purpose:** Classify whether the S&P 500 will rise or fall the next day
- **Features Used:**
  - Previous daily returns (lags)
- **Target Variable:**
  - Binary (Up / Down)

The model estimates:

\[
P(\text{Up}) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X_1 + \beta_2 X_2 + \dots)}}
\]

Where \( X_i \) are lagged returns.




