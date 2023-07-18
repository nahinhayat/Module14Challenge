Module 14 Challenge

Description:

In this challenge I created an alogrithmic trading model using machine learning to predict trading signals. I created the model with the SVC classifier model, and then with DecisionTreeClassifer as well. This was done to predict the best points to buy and sell a stock.

Details:

It begins with creating a algorithmic trading model that uses when the daily return percentage is positive as an entry point and negative as exit point. I honestly do not understand why we find the short and long SMAs because we do not use them at all during this process. The signals are based on solely the actual returns column created from the daily percentage change of the closing price.

![screenshot1]()

Next we prepare the data to be used in a machine learning model by creating sets for features and targets, select periods for training, generate test and train datasets, scale the features, git the model and ultimately predict signals

![screenshot2]()

I then began an attempt to tune the algorithm. I began by changing the training window to nine months instead of three months. This resulted in the model being less accurate.

![longerwindowsvmrun]()

Next I tried changing the long window SMA slow window to thirty days instead of one hundred days and this actually made the results more accurate. Which leads me to believe the best set of parameters would be to keep the training window at three months but changing the SMA slow window to smaller amount of days. I actually messed with the SMA windows before I landed at this decision because the options would not even show up on the plot. 

![differentSMAwindowsvmrun]()

I also used the DecisionTreeClassifier model but this model was not as accurate as SVC.

![screenshotlike5]()


Author: Nahin Hayat https://www.linkedin.com/in/nahinhayat/