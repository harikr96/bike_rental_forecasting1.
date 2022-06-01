# bike_rental_forecasting1.
Using weather data and historical usage patterns, forecast the hourly bike rental demand.  Using Linear regression model and Decision tree model. 

# Problem statement

Bike sharing systems are a means of renting bicycles where the process of obtaining membership, rental, and bike return is automated via a network of kiosk locations throughout a city. Using these systems, people are able to rent a bike from one location and return it to a different place on an as-needed basis. Currently, there are over 500 bike-sharing programs around the world.

The data generated by these systems makes them attractive for researchers because the duration of travel, departure location, arrival location, and time elapsed is explicitly recorded. Bike sharing systems therefore function as a sensor network, which can be used for studying mobility in a city. 


In this project, we are asked to combine historical usage patterns with weather data in order to forecast hourly bike rental demand. 


Here is the description of all the variables : 
 

Variable                                  Definition 

datetime                                  hourly date + timestamp 

season                                    Type of season (1 = spring, 2 = summer, 3 = fall, 4 =                                                                                                 winter) 

holiday                                   whether the day is considered a holiday 

workingday                                whether the day is neither a weekend nor holiday 

weather                                   weather 

temp                                      temperature in Celsius 

atemp                                     "feels like" temperature in Celsius 

humidity                                  relative humidity 

windspeed                                 wind speed 

casual                                    number of non-registered user rentals initiated 

registered                                number of registered user rentals initiated 

count                                     number of total rentals 


# Tools and libraries used:

Jupyter notebook, Python(NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn, SciPy, Calender , datetime)


# Machine learning algorithm used :

1.Linear regression:

   Rmsle Value:    0.8876469542289628

     rmsle value should be close to 0 for an efficient model but her it's not so lets try other models.
 
2. Decision tree:
   
   Rmsle    = 0.17134338947669225

      rmsle value is close to 0 which means our model efficiency has increased.





# Inference from the Exploratory data analysis:


1. Summer is the dominating season.

2. working day has higher chance for rentals

3. highest count was on 2012-03-23 17:00:00 in summer. majority of them were registered.

4. Hours having only 1 rental of bikes per hour(least rental) are 104 hours were for season            1=spring ,28 hours for summer,6 hours for fall,11 hours for winter

6. Average temperature is about 19.72

7. Summer season contributes most of the time followed by spring

8. Temp rangin from 10 to 30 constitute most of the data

9. 40 to 90 is the frequently occuring humidity.

10. Frequently occuring windspeed is between 5-20

11.The logrithmatic distribution plot of count is a left skewed distribution plot.

12.50% of the humidity lies from 7 to 19.001.

13.season 2 and 3 (summer and fall) have higher counts and counts on holiday and working day are   
comparable.

14.for summer and fall ,count is higher for weather 1 followed by 2&3 but for weather 4 its =0 for    summer ,fall,and 

15.if its holiday and the weather is 4 the count is null which indicates poor demand for rental at    that time

16.For weather 4 only season 1(spring) has demand for rental bike. As for we can reduce the operational cost during other season.

17.Relation between registerd and count clearly has a linear relationship. So as the registered customers increases there is a high chance of increased demand in rental of bikes

18. As casual customers increases the rentals also increases

18. insights from correlation chart:

     1. temp and humidity features has got positive and negative correlation with count 
     
     respectively.Although the correlation between them are not very prominent still the count 
      
      variable has got little dependency on "temp" and "humidity".

    2. windspeed will not be really useful numerical feature and it is visible from it correlation 
    
       value with "count"

    3. Since "atemp" and "temp" has got strong correlation with each other, during model building 
    
       any one of the variable has to be dropped since they will exhibit multicollinearity in the          data










 
