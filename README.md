# python-api-challenge

Executive Summary


The key findings of the WeatherPy analysis is that there does seem to be some sort of relationship between Latitude and  Max Temp (F), Wind Speed, Humidity, and Cloudiness respectively. That relationship seeminginly depends on the distance from the 0 mark in latitude - the equator. When going farher south into negative latitudes, or further north, the conditions seem to change moderately. 

The VacationPy analysis helped me decide where I will be taking my next sun drenched vacation. The hotel_df that was created during that analysis contains a list of locations that have low cloud cover and are fairly warm. The analysis is meant to also find me the nearest hotel within 10 kilometers to the assigned latitude and longitude for the city so I have an idea of where to stay.


Introduction


The purpose of this analysis is to better understand how to use regressions, plots, and other tools to determine the relationship between certain peices of information. In this case we were looking at different weather conditions (Max Temps (F), Cloudiness, Humidity, Wind Speed (m/s)) and examining the effect that different latitudes may have on those weather conditions. 

I was then asked to use this analysis to find my ideal weather destinations. Once I had those locations I was able to create a request to find the nearest hotel for the respective cities. 


Data Collection and Preparation


Data collection for WeatherPy: The list of locations for this assignment was created by gathering a list of random latitude and longitudes then locating the nearest city to those locations. Once I had that list of cities, I created an API request to gather the earlier mentioned weather conditions and place them into a DataFrame - city_data_df - with their corresponding city and coordinates. With that information I created linear regression models for each condition against the latitudinal position of their respective city. 

Data Collection for VacationPy: I used the data from the city_data_df and narrowed down the locations based off criteria that I specified. Once I had this data I prepared an API request that would provide me with the nearest hotel to the location coordinates provided. 



Data Analysis


First off, I had to create a list of random latitudinal and longitudinal positions then ran an API request to get different weather conditions (Max Temps (F), Cloudiness, Humidity, Wind Speed (m/s)) for each city nearest to the randomized location. I created a DataFrame with the weather conditions listed and began running a regression for each of the variables against the city's Latitude. Once that was completed for each variable, I set out to narrow down the DataFrame to locations I feel had the right criteria for a vacation. 


Conclusion


When analyzing the regressions that I created in WeatherPy, it appears that the distance from the equator - north or south - has an effect on the various weatehr variables. The closer to the equator a location was, the higher the Max Temps (F) tended to be as well as Humidity levels. Meanwhile, the further from the equator a location was the more likely it was to have higher Wind Speeds (m/s). 

I was able to use this data on the second part of the assignment to create a list of locations that I would find suitable for a vacation after this class is completed. I felt like a relaxing sun-filled vacation was in order so I narrowed down the list to warmer locales and then ran the API request to get the nearest hotel to the city. 

I had issues creating the map plots due to some dependencies not having downloaded properly. Due to that my Humidity map is not available and I believe that would have helped create a clearer picture about the rlationship between Humidity and Latitude. 
