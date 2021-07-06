# StockPredictor

Investment firms, hedge funds and even individuals have been using financial models to better understand market behavior and make profitable investments and trades. A wealth of information is available in the form of historical stock prices and company performance data, suitable for machine learning algorithms to process.

Investors make educated guesses by analyzing data. They'll read the news, study the company history, industry trends and other lots of data points that go into making a prediction. The prevailing theories is that stock prices are totally random and unpredictable but that raises the question why top firms like Morgan Stanley and Citigroup hire quantitative analysts to build predictive models.

Machine learning has significant applications in the stock price prediction. In this machine learning project, we will be talking about predicting the returns on stocks. This is a very complex task and has uncertainties.

This project utilizes Deep Learning models, Long-Short Term Memory (LSTM) Neural Network algorithm, to predict stock prices. For data with timeframes recurrent neural networks (RNNs) come in handy but recent researches have shown that LSTM, networks are the most popular and useful variants of RNNs. 

I have used Keras to build a LSTM to predict stock prices using historical closing price and trading volume and visualize both the predicted price values over time and the optimal parameters for the model.


## Problem Highlights
*The challenge of this project is to accurately predict the future closing value of a given stock across a given period of time in the future.  For this project I have used a Long Short Term Memory networks – usually just called “LSTMs” to predict the closing price of the S&P 500 using a dataset of past prices*

## Project

Get the Data

In the following cells we download and save the S&P 500 dataset.

Step 1 : Define a function to get historical data from google finance

Step 2: Get the data of desired firm from Google Finance.

Step 3: Write the data to a csv file.



Preprocess the data

Now it is time to preprocess the data. In the following cells we will normalise it for better prediction of data.

Step 1 : Get the data from csv file.

Step 2 : Remove Unncessary data, i.e., Date and High value and Visualise raw data.

![image](https://user-images.githubusercontent.com/56619771/124559876-ce540300-de59-11eb-9e2e-639870b54d31.png)

Step 3 : Normalise the data using minmaxscaler function

Step 4 : Visualize the data again

![image](https://user-images.githubusercontent.com/56619771/124560154-212dba80-de5a-11eb-8fe2-aeb39505f2d1.png)

Step 5: Log the normalised data for future resuablilty



Bench Mark Model

In this section we will check our bench mark model. As is proposed in my proposal my bench mark model is a simple linear regressor model.

Step 1: Load the preprocessed data

Step 2: Split data into train and test pair

Step 3: Train a Linear regressor model on training set and get prediction

Step 4: Get prediction on test set

Step 5: Plot the predicted values against actual

![image](https://user-images.githubusercontent.com/56619771/124560388-605c0b80-de5a-11eb-8196-5d85b9e52d97.png)

Step 6: measure accuracy of the prediction



Long-Sort Term Memory Model

In this section we will use LSTM to train and test on our data set.


Basic LSTM Model

First lets make a basic LSTM model.

Step 1 : import keras libraries for smooth implementaion of lstm

Step 2 : Split train and test data sets and Unroll train and test data for lstm model

Step 3 : Build a basic Long-Short Term Memory model

Step 4: Train the model

Step 5: make prediction using test data

Step 6: Plot the results

![image](https://user-images.githubusercontent.com/56619771/124560982-027bf380-de5b-11eb-89c4-0908e7df238b.png)

Step 7: Get the test score.



Improved LSTM Model

Step 1: Build an improved LSTM model

Step 2: Train improved LSTM model

Step 3: Make prediction on improved LSTM model

Step 4: plot the results
![image](https://user-images.githubusercontent.com/56619771/124561155-348d5580-de5b-11eb-96ab-ec5738f71b20.png)

Step 5: Get the test score



Checking Robustness of the model

In this section we will check robustness of our LSTM model. I have used new unseen datasets for this from July 1, 2017 to July 20,2017. I have downloaded the data sets from google finance website to check for robustness of the model.

Test Score: 0.3897 MSE (0.6242 RMSE) is the test score i got for this model.



## Software and Libraries
This project uses the following software and Python libraries:

* [Python 2.7](https://www.python.org/download/releases/2.7/)
* [NumPy](http://www.numpy.org/)
* [pandas](http://pandas.pydata.org/)
* [Keras](https://keras.io/)
* [Tensor-flow](https://www.tensorflow.org)
* [Jupyter Notebook](http://ipython.org/notebook.html)

