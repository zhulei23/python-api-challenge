Python-API-Challenge:

Part I - WeatherPy
Challenge/Task:
First requirement is to create a series of scatter plots to showcase the following relationships:

1. Temperature (F) vs. Latitude
2. Humidity (%) vs. Latitude
3. Cloudiness (%) vs. Latitude
4. Wind Speed (mph) vs. Latitude

Second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

1. Northern Hemisphere - Temperature (F) vs. Latitude
2. Southern Hemisphere - Temperature (F) vs. Latitude
3. Northern Hemisphere - Humidity (%) vs. Latitude
4. Southern Hemisphere - Humidity (%) vs. Latitude
5. Northern Hemisphere - Cloudiness (%) vs. Latitude
6. Southern Hemisphere - Cloudiness (%) vs. Latitude
7. Northern Hemisphere - Wind Speed (mph) vs. Latitude
8. Southern Hemisphere - Wind Speed (mph) vs. Latitude

Three osbervable trends:
1. The scatter plot of City Latitue vs. Max Temprature indicates that the temperature closes to equator has the highest temperature. The further the latitude from the equator, the lower the temperautre is. 
2. The changes of the Latitude does not impact the Humidity, Cloudiness, and Wind Speed heavily as the data shows all three elements are spreaded cross the Latitude evenly.
3. There is not strong relationship between Humidity & Latitude for both Northern & Southern Hemisphere; however, the Northern Hemisphere shows larger cluster comparing to Southern Hemisphere which is higher than 60%. 

Process for running script:
1. Perform API Calls
* Print statement to start run the API Calls
* Save config information
* Build partial query URL
* Set up lists to hold response info
* Set initial count number for the API call loop
* Loop through the list of cities and perform a request for data on each
* Add if condition for the count
* Print statement for processing records
* Add Exception Handling message for City not found
* Print statement for ending the process
* Create a DataFrame to hold retrieved variables
* Export the city data into a .csv file
* Display the DataFrame

2. Temperature (F) vs. Latitude
* Count of retrieved city data
* set up x_values & y_values
* set up formatting for scatter plot
* set up scatter title, xlabel, and ylabel
* save fig & show final result

3. Humidity (%) vs. Latitude
* same process as item 2

4. Cloudiness (%) vs. Latitude
* same process as item 2

5. Wind Speed (mph) vs. Latitude
* same process as item 2

1. Northern Hemisphere - Temperature (F) vs. Latitude
* set up x_values & y_values
* set up formatting for scatter plot
* set up scatter title, xlabel, and ylabel
* save fig & show final result

2. Southern Hemisphere - Temperature (F) vs. Latitude
* same process as item 1

3. Northern Hemisphere - Humidity (%) vs. Latitude
* same process as item 1

4. Southern Hemisphere - Humidity (%) vs. Latitude
* same process as item 1

5. Northern Hemisphere - Cloudiness (%) vs. Latitude
* same process as item 1

6. Southern Hemisphere - Cloudiness (%) vs. Latitude
* same process as item 1

7. Northern Hemisphere - Wind Speed (mph) vs. Latitude
* same process as item 1

8. Southern Hemisphere - Wind Speed (mph) vs. Latitude
* same process as item 1

Part II - VacationPy

Challenge/Task:
1. Sort Part I results into DataFrame
* Load the weatherpy_data.csv file
* Create a dataframe with imported csv file
* Display dataframe

2. Humidity Heatmap
* Configure gmaps
* Count current total records for the new dataframe
* Drop NaN values on the dataframe
* Use the Lat & Lng as locations
* Use Humidity as the weight
* Create a Humidity heatmap

3. Create new DataFrame fitting weather criteria
* Create a new dataframe for ideal weather conditions
* Adding condition of max temperature higher than 70 degrees
* Adding condition of max temperature lower than 80 degrees
* Adding condition of wind speed less than 10 mph
* Adding condition of zero cloudiness
* Drop any rows that don't contain all three conditions
* Reset index number on the new dataframe

4. Plot the hotels on top of the humidity map
* Store into variable named hotel_df
* Add a "Hotel Name" column to the DataFrame.
* Set variable for searching for hotel names
* Set parameters to search for hotels with 5000 meters
* Use the Lat & Lng to identify hotels
* Retrieve Lat & Lng from hotel dataframe
* Change location each iteration while leaving orginal params in place
* Set up base_url
* Make request and print url
* Store the first Hotel result into the DataFrame
* Create message to skip missing data and keep loop running
* Append searched hotel names to dataframe
* Display complete result
* Create clean dataframe by removing NaN records
* Select top 8 cities with minimum humidity 
* Reset index number for selected records
* Using the template add the hotel marks to the heatmap
* Add marker layer ontop of heat map
* Add the layer to the heat map
