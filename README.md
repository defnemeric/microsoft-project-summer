# Microsoft Summer 2025 Internship Project: Stock Price Prediction using LSTM

## Overview
This project is developed by **Defne Meric Erdogan** as part of the **Microsoft Turkey Summer Internship AI Innovators Program**.

## Motivation
The main goal is to apply machine learning techniquest to real world financial data, and explore predictive capabilities in stock market analysis.

## Project Description
This project focuses on developing a stock price prediction model using a type of RNN called LSTM (Long Short-Term Memory) neural network built in PyTorch and optimized with Optuna.

## Dataset
The dataset used in this project provides the history of daily prices of Microsoft Stock(MSFT). 
- The fields include:
    - open
    - high
    - low
    - close -> target value we want to predict
    - adj close
    - volume


## Project Structure
- README.md: Project description documentation.
- MSFT.csv: The dataset of Microsoft stock prices.
- stock-prediction-pytorch.ipynb: Jupyter notebook that consists of data analysis, LSTM model building, training, evaluation, data exploration, and interpretation of the results
- imaegs folder: The training and evaluation results displayed as plots

## Model Architecture

- LSTM neural network with tunable hyperparameters:
  - `hidden_dim`: number of hidden units
  - `num_layers`: number of LSTM layers
  - `learning_rate`: optimizer learning rate
  - `batch_size`: batch size for training

## Training Strategy
- Normalization with `MinMaxScaler`
- Sequence windowing with a lookback period of 30
- Train/validation split
- Early stopping to prevent overfitting
- Loss function: MSE (Mean Squared Error)

## Results
MSE (Mean squared error) is used for model evaluation. Model performs better in training dataset compared to the test dataset which results from overfitting of the model. Detailed results are in the stock-prediction-pytorch.jpynb notebook.

## Installation and Usage
To get started with the code, run the following on your terminal:
~~~
git clone https://github.com/defnemeric/microsoft-project-summer
cd microsoft-project-summer
pip install -r requirements.txt
~~~
1) Make sure MSFT.csv is placed in the project root directory.
2) Create a virtual environment and download the requirements
2) Run stock-prediction-pytorch.ipynb to preprocess data, train the LSTM model, and evaluate predictions.

## Sample Output
Here is an example plot showing the LSTM model’s predicted stock price vs. the actual Microsoft stock price:

![LSTM Prediction](images/lstm_prediction.png)

## Author
Defne Meric Erdogan [LinkedIn](https://www.linkedin.com/in/defne-meric-erdogan/) | defnem.erdogan@gmail.com

## Acknowledgments
Special thanks to Barbaros Gunay for his mentorship and guidance throughout the program.

Dataset: Verma, Arpit. (2022). Microsoft Stock Data. Retrieved July 16 2025 from https://www.kaggle.com/datasets/varpit94/microsoft-stock-data
