# Flight-Delay
Airlines try to avoid flight delays as much as possible to avoid the associated costs related to the insurance charges and the cascading effects on their service as well as their public impression. As such, predicting flight delays can help airlines, airports, passengers and insurance companies for schadueling, decision making and allocating resources. This project aims for developing machine learning model(s) for predicting flight delays based on several pre-flight data, including: previous delays and weather.

According to the US Bureau of Transportation Statistics, the main causes of the flight delays include: National Aviation System, extreme weather condition, previous flight delays and security delays:

<img src="/Images/Image1.png">

The dataset for this study includes the record of various components of the delays related to daily flights in the US for the years 2018-19. The key characteristics of this dataset is: it is very large, the delay problem seems to be very stochastic and we should keep in mind that only the pre-flight data can be used for prediction (i.e. not all the fields in the dataset can directly be considered as a feature.)

I have done an extensive exploratory data analysis on the dataset - presented in the notebooks "EDA1" to "EDA6" - to better understand the data and get help in developing hypotheses. Some noticeable results are:

Unlike what one may think, the mean delay is zero (e.g. no delay) and in fact, a considerable portion of flights arrive earlier than what is shcadualed (e.g. negative delay) but there are certainly some outlier i.e. very large delays.

<img src="/Images/Image2.png">

The data shows that most of delays have already happenned before departure and surprisingly, some of the delays are compensated during the flight i.e. the aircrafts fly faster!

Also, there are some variation in the delay data throught the year but it is hard to associate the delays to a seasonal pattern (e.g. to the season's weather or holidays):

Given the size of the dataset and stochastic nature of the problem (e.g. changing the delay dynamic over time and the cascading effect), I am developing an online model - which keeps updating itself. For this reason, I have developed a feature named as : averaged recent tail-number delays which tracks back the delays of the same tail-number for 1 week. Unlike many other features that I have tried, this new feature shows promising correlation with the target variable and increases the training score to ~50%: 

<img src="/Images/Image3.png">

I am still working on this problem using RandomForest machine learning model and am trying to develop more features based on the idea of dynamic time-averaging.
You can find the current modeling in "Main" notebook. The online modeling approach that I use involved several sampling from the dataset using PostgeSQL queries from a private database which, unfortunately, I cannot share. But I will provide a sample of the data in near future on this repo. 

Interested or have questions? Please don't hesitate to comment here or contact me. Also, feel free to fork and contribute to the project...




Given the size of the dataset  online method using dynamic time-averaging is used to engineer features to improve he predictions considering the highly-stochastic nature of the problem...

<img src="/Images/Image4.png">


Interested or have questions? Please don't hesitate to comment here or contact me. Also, feel free to fork and contribute to the project...
