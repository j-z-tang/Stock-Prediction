# Predicting stock prices with Machine Learning - Udacity Data Science Nanodegree Capstone Project

## Project overview
The ability to predict movement of stock prices has been the Holy Grail for investors around the world.  In this project, we explore the topic of predicting the movement of stock prices using supervised learning, as well as more sophisticated deep learning methods.

We will discuss in detail steps taken to obtain and visulise historical data, background of each learning method used, and evaluation of the performance of each model against 8 heavily traded stocks in Hong Kong and US stock exchanges.  The 4 methods we will explore in here are SVM, Random Forrest, XGBoost, and Deep Learning with LSTM and CNN.

Full discussion of this project can be found on the blog page [here.](https://jztang.medium.com/predicting-stock-prices-with-ai-which-method-should-you-use-to-profit-5cbc4c9a2cc1)

## Problem Statement
We seek to explore the use of machine learning for the following two problems, with the first being a simplified version of the second:
1. Can we used to classify whether a particular stock price would increase or decrease on a particular day, given observations of several preceding days' trading conditions?
2. Can we make use of Classical ML and more sophisticated Deep Learning techniques to predict the closing price (and therefore profit) of the next trading day?


## Approach

The following outlines the approach taken to address our problem statement.

1. Extract and Explore data:
    - We use data from Yahoo Finance, where we extract daily trading data from the past 10 years, including: how many stocks were traded (Volume) and closing price adjusted for stock splits (Adjusted Close)
    
    
2. Feature engineering
    - We engineer new features from our trading dataset to aid with model training, including rolling means, rolling stdev, rolling upper/lower bounds of prices.


3. Data Preparation
    - We prepare our data including splitting of training and testing sets


4. Modelling & Evaluation
    - Classification of rise / fall in an unseen day
    - Regression and Deep Learning models for price change in an unseen day
    
    
5. Conclusion


    
## Metrics

The performance of model will be judged by its ability to predict actual stock price.

For Problem Statement 1, we will assess the model by the accuracy with which it can classify a rise or fall in stock price on an unseen trading day, as measured by % of correctly classified days.

For Problem Statement 2, we will assess the model by the accuracy with which it can predict the actual profit from holding a stock for an unseen trading day, as measured by mean-squared-error.

## Libraries Used & Acknolwedgements

We have made extensive use of the following libraries.  Please refer to the licensing terms therein.
- yFinance
- Pandas
- Numpy
- TensorFlow
- Scikit-Learn
- Matplotlib
