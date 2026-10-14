# AI-Based Financial Time Series Forecasting

## Reliance Stock Price Prediction using LSTM

This project demonstrates financial time-series forecasting using a Long Short-Term Memory (LSTM) neural network.

The model uses historical Reliance stock closing prices to learn temporal patterns and predict the next day's closing price.

## Features

* Historical stock dataset loading
* Date conversion and sorting
* Close price extraction
* Min-Max normalization
* Time-series sequence creation
* LSTM input reshaping
* LSTM gate concept demonstration
* Train-test split
* LSTM model training
* Early stopping
* Stock price prediction
* MAE, MSE and RMSE evaluation
* Actual vs predicted visualization
* Training and validation loss visualization
* Next-day closing price prediction
* Model and prediction output saving

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow
* Keras
* LSTM

## Project Architecture

```text
Historical Stock Data
        ↓
Date Conversion & Sorting
        ↓
Close Price Extraction
        ↓
Min-Max Scaling
        ↓
Create 10-Day Sequences
        ↓
Reshape Data for LSTM
        ↓
Train-Test Split
        ↓
LSTM Model
        ↓
Model Training
        ↓
Test Data Prediction
        ↓
Inverse Scaling
        ↓
MAE / MSE / RMSE
        ↓
Actual vs Predicted Graph
        ↓
Next-Day Price Prediction
```

## Dataset

The project uses a CSV file named:

```text
marvellous_reliance_stock_sample.csv
```

The dataset should be kept in the same directory as the Python program.

The model uses the `Close` price for forecasting.

## LSTM Model

The model contains:

* LSTM layer with 50 units
* Dropout layer with 20% dropout
* LSTM layer with 50 units
* Dropout layer with 20% dropout
* Dense layer with 25 neurons
* Output Dense layer with 1 neuron

The model uses:

* Optimizer: Adam
* Loss: Mean Squared Error
* Maximum Epochs: 60
* Batch Size: 16
* Validation Split: 20%
* Early Stopping Patience: 10

## Time-Series Sequence

The model uses the previous 10 days of closing prices to predict the next day's closing price.

```text
Day 1 ─┐
Day 2  │
Day 3  │
...    ├──→ LSTM ──→ Next Day Close Price
Day 9  │
Day 10 ┘
```

## Evaluation Metrics

The model is evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

## Output

When the program runs, it produces:

* Dataset information
* Scaled values
* Time-series sequences
* LSTM model summary
* Training progress
* Predictions
* MAE, MSE and RMSE
* Actual vs predicted stock price graph
* Training loss graph
* Next-day predicted closing price

The program also saves:

```text
marvellous_actual_vs_predicted_detailed.png
marvellous_training_loss_detailed.png
marvellous_reliance_lstm_detailed_model.h5
marvellous_reliance_prediction_output.csv
```

## Installation

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Reliance-LSTM-Time-Series
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the Project

```bash
python 48_Reliance_LSTM_Time_Series.py
```

## Important Note

This project is for educational purposes and demonstrates LSTM-based time-series forecasting.

Stock-price predictions are inherently uncertain and should not be treated as financial advice.

## Concepts Covered

* Time-Series Forecasting
* LSTM Neural Networks
* Recurrent Neural Networks
* Min-Max Scaling
* Sequence Generation
* Backpropagation Through Time
* Early Stopping
* Regression
* Model Evaluation
* Data Visualization

## Author

Avantika Kedari
