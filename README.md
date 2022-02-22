# Flight-Delay
Airlines try to avoid flight delays as much as possible to avoid the associated costs related to the insurance charges and the cascading effects on their service as well as their public impression. As such, predicting flight delays can help airlines, airports, passengers and insurance companies for schadueling, decision making and allocating resources. This project aims for developing machine learning model(s) for predicting flight delays based on several pre-flight data, including: previous delays and weather.

According to the US Bureau of Transportation Statistics, the main causes of the flight delays include: National Aviation System, extreme weather condition, previous flight delays and security delays:

<img src="/Images/Image1.png">

The dataset for this study includes the record of various components of the delays related to daily flights in the US for the years 2018-19. The key characteristics of this dataset is: it is very large, the delay problem seems to be very stochastic and we should keep in mind that only the pre-flight data can be used for prediction (i.e. not all the fields in the dataset can directly be considered as a feature.)

I have done an extensive exploratory data analysis on the dataset - presented in the notebooks "EDA1" to "EDA6" - to better understand the data and get help in developing hypotheses. Some noticeable results are:

<img src="/Images/Image2.png">



<img src="/Images/Image3.png">





Given the size of the dataset  online method using dynamic time-averaging is used to engineer features to improve he predictions considering the highly-stochastic nature of the problem... 
