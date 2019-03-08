# crime-weather-chicago

Finding the correlation between crime and weather in chicago.

Hypothesis: The higher the temperature and/or lower the precipitation, the more amount of crimes committed

Used pyspark and dynamodb on the back end and HTML, CSS, and JavaScript on the front end. 

Models used
- Linear Regression
- Gradient-Boosted Tree Regression
- Decision Tree Regression
- Random Forest Regression
- K-Means Clustering

Screenshots
![Imgur](https://i.imgur.com/xV332qP.png)
![Imgur](https://i.imgur.com/VfPqSdR.png)
![Imgur](https://i.imgur.com/8hvNS0M.png)
![Imgur](https://i.imgur.com/jZuLsFz.png)

Conclusion
- After applying the various models onto the data, there is some correlation between weather and crime, but not very strong
- Relatively, temperature has a noticeably greater effect on crime than precipitation, sporting a ~2.2% statistical significance vs ~-0.1% for precipitation
