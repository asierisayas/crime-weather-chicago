# Crime Weather Chicago

I recently visited Chicago and during my trip back to Atlanta I was remembering a conversation 
I had with a local about Chicago's crime rate. She said that the crime rate lowered starting in late 2018 
compared to the previous part of the year. I started to wonder if there was a correlation between crime and weather 
so here goes :)

# Hypothesis
My guess is the higher the temperature and/or lower the precipitation, the more amount of crimes are committed.
Below you'll find my approach.

### Crime data set
- Found a CSV file on kaggle
- Was an extensive dataset of reported crimes in Chicago from 2004 til present

### Weather data set
- Retrieved from OpenWeatherAPI saved locally as a CSV
- Data is from Jan 1st 2005 til Feb 10th 2019

### Storing the Data
- DynamoDB
- Enumerate function used to extract data from CSV
- Both the Weather and Crime dta put into DynamoDB

### Spark
- PySpark - Spark Python API that deploys the Spark programming model to Python
- Enabled the weather and crime data to be split into distributed datasets for faster processing and interpretation
- Models Used
  * Linear Regression
  * Gradient-Boosted Tree Regression
  * Decision Tree Regression 
  * Random Forest Regression 
  * K-Means Clustering
  
### Data Flow
1. DynamoDB
2. Lists
3. Combine List based on Date
4. Parallelize data onto a RDD (start spark session)
5. Label data onto data frame (models run on data)

Here are some screenshots of my findings
![Imgur](https://i.imgur.com/8hvNS0M.png)
![Imgur](https://i.imgur.com/jZuLsFz.png)
![Imgur](https://i.imgur.com/VfPqSdR.png)
![Imgur](https://i.imgur.com/xV332qP.png)

## Conclusion
- After applying the various models onto the data, there is some correlation between weather and crime, but not very strong
- Relatively, temperature has a noticeably greater effect on crime than precipitation, sporting a ~2.2% statistical significance
vs ~0.1% for precipitation
