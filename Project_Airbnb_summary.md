### Project 2 summary

## Predicting the rate of Airbnb rental

Katrina Bykova

----------------------------------------------------------------------------------------------------------------

**Introduction**

​	Airbnb is webservice that brings together property owners who are willing to rent out their homes and guests who need a place to a stay.

​	The goals of this project were 1) to estimate a property overnight rental rate based on the information available on Airbnb websitefind and 2) to identify factors that have the most effect on Airbnb overnight rates in Seattle.

**Data and tools**

​	Data about properties listed on Airbnb website for Seattle, WA were collected with Selenium package (~1,200 properties). Additional information about Seattle neiborhoods was found from Wikipedia. Property addresses were located from Airbnb coordinates  with GeoPy package. The addresses subsequently were used to extract neighborhood information for each listed property.

**Results**

​	Linear regression was used to fit the collected data. Logarithmic tranformation of the target variable improved the regression model whereas neither power transformation nor polynomial transformation had no effect on R-squared values. 

​	Models with regularization methods (Ridge, Lasso, Elastic Net) performed as well or worse as a slimple regression with no penalty for the model complexity. 

​	Feature reduction via regression model coefficients and recursive feature elimination resulted in a reduction of dimensioanality from 34 to 20 without a decrease in the model performance.

​	Simulated property data set (~50,000 observations) was built based on the features present in the Airbnb data set that was used to built the regression models. Rental rates for the simulated set were predicted using the selected regression model. Feature importance was explored with the simulated data set. 

​	The most important feature for the rental rate was location within a specific Seattle neiborhhod. Another feature with a significant effect on the overnight rate was the number of beds in a given property. Number of bathrooms and bedrooms (studio and up to 2 bedrooms) were not as significant.

**Recommendations**

​	Property owners might want to increase the number of sleeping places in their rental homes to increase the overnight rate. Choosing a location with a higher rental price is another way to increase the revenue if that option is available.

​	Guests on the other hand might want to be conscious of the neighborhood they are renting a property in. More affordable neighborhoods can be available if a specific location within Seattle is not as important. Bringing an air mattress is another way to reduce expenses for guests. Maximum occupancy should be kept in mind.

**Additional questions**

​	Next level of questions requires additional data and models to be built. How does Airbnb compare to its's competitor VRBP? Does the property value correlate with the rental rate?







