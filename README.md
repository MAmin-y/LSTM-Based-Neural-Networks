# Spam Detection and Oil Price Forecasting Project

Below are detailed explanations for each part of the project.

## Part 1: Spam Detection in Persian Emails

In the first part of this project, a model is developed to classify Persian emails as spam or non-spam. This project is inspired by the paper "A Hybrid CNN-LSTM Model for SMS Spam Detection in Arabic and English Messages" (refer to the [MDPI](https://www.mdpi.com/1999-5903/12/9/156) for further details). The process begins by acquiring a dedicated dataset from Kaggle containing Persian spam emails, followed by an exploratory analysis to visualize the distribution of spam and non-spam messages through bar charts. The text data is then meticulously preprocessed: noise such as URLs, email addresses, phone numbers, and excessive character repetitions are removed to improve the signal quality. Advanced text cleaning techniques are applied, including the normalization of characters and removal of stop words. Next, the cleaned text is converted into numerical form using ParsBERT embeddings, which not only provide a dense representation of the text but also preserve semantic similarities between words. A CNN-LSTM hybrid architecture is subsequently designed to capture both spatial features (through convolutional layers) and sequential patterns (through LSTM layers) within the text. The model is trained on the processed dataset with careful tuning of hyperparameters such as batch sizes, learning rates, and optimizers (e.g., Adam and SGD). The performance is then evaluated using standard metrics including accuracy, precision, recall, and F1-score, with a comparative analysis against traditional bag-of-words approaches to highlight the benefits of using deep contextual embeddings.

## Part 2: Oil Price Forecasting Using ARIMA and Deep Learning Models

The second part of the project focuses on forecasting crude oil prices using historical data from Yahoo Finance. The dataset consists of the 'Adj Close' prices for crude oil (CL=F) starting from 2010, with deliberate introduction of missing values to reflect realistic data challenges. Initially, the data undergoes rigorous preprocessing, including imputation of missing values, normalization, and splitting into training and testing subsets. This section explores two main forecasting strategies: deep learning models and classical statistical methods. On the deep learning side, models such as GRU, LSTM, and Bi-LSTM are implemented to capture complex temporal dependencies in the time series data, and their performances are assessed using evaluation metrics like MAE, RMSE, MAPE, and R-squared. In parallel, a traditional ARIMA approach, along with Seasonal ARIMA (SARIMA), is employed to model the autoregressive and moving average components of the time series. Inspired by the paper "Oil Price Forecasting: A Comparative Study Using Deep Learning and ARIMA Models" (refer to the [ESJ article](https://www.ijournalse.org/index.php/ESJ/article/view/2149) for further details), the project carefully compares the strengths and limitations of these methodologies. Detailed parameter tuning, model evaluation, and visualizations of forecasting performance are provided, leading to insights on the trade-offs between deep learning and classical time series forecasting methods.
