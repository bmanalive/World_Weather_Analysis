# World_Weather_Analysis

Background
Jack loves the PlanMyTrip app. Beta testers love it too. And, as with any new product, they’ve recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data you’ve already retrieved in this module. Then, you'll have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, you will create a travel route between the four cities as well as a marker layer map.

What You're Creating
This new assignment consists of three technical analyses. You will submit the following deliverables:

Deliverable 1: Retrieve Weather Data
Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap. In addition to the city weather data you gathered in this module, use your API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.

Deliverable 2: Create a Customer Travel Destinations Map
Use input statements to retrieve customer weather preferences, then use those preferences to identify potential travel destinations and nearby hotels. Then, show those destinations on a marker layer map with pop-up markers.

Deliverable 3: Create a Travel Itinerary Map
Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.


Files
Use the following links to download the Challenge starter codes.

Download Deliverable 2 starter code (Links to an external site.)

Download Deliverable 3 starter code (Links to an external site.)

-------------------------------------------------------------------------
Deliverable 1: Retrieve Weather Data (25 points)
Deliverable 1 Instructions
Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap. In addition to the city weather data you gathered in this module, use your API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.

REWIND
For this deliverable, you’ve already done the following in this module:

Lesson 6.2.3: Make an API call
Lesson 6.2.3: Create a config.py file
Lesson 6.2.6: Retrieve city weather data
Lesson 6.2.7: Add the weather data to a DataFrame
Lesson 6.2.7: Export the DataFrame to a CSV file
Create a folder called Weather_Database.

Create a new Jupyter Notebook file to retrieve the weather data, and name it Weather_Database.ipynb.

Create a new set of 2,000 random latitudes and longitudes.

Get the nearest city using the citipy module.

Perform an API call with the OpenWeatherMap.

Retrieve the following information from the API call:

Latitude and longitude
Maximum temperature
Percent humidity
Percent cloudiness
Wind speed
Weather description (for example, clouds, fog, light rain, clear sky)
Add the data to a new DataFrame.

Before exporting your new DataFrame as a CSV file, take a moment to confirm that it looks similar to the image below:
The new cities_data DataFrame summarizes the current weather description.

Export the DataFrame as a CSV file, and save it as WeatherPy_Database.csv in the Weather_Database folder.

Deliverable 1 Requirements
You will earn a perfect score for Deliverable 1 by completing all requirements below:

Retrieve all of the following information from the API call: (15 pt)

Latitude and longitude
Maximum temperature
Percent humidity
Percent cloudiness
Wind speed
Weather description (for example, clouds, fog, light rain, clear sky)
Add the weather data to a new DataFrame (5 pt)

Export the DataFrame as WeatherPy_Database.csv into the Weather_Database folder (5 pt)

Be sure to double-check that you have the following in the Weather_Database folder:

The Weather_Database.ipynb file
The WeatherPy_Database.csv file

---------------------------------------------------------------------------------------------------
Deliverable 2: Create a Customer Travel Destinations Map (35 points)
Deliverable 2 Instructions
Use input statements to retrieve customer weather preferences, then use those preferences to identify potential travel destinations and nearby hotels. Then, show those destinations on a marker layer map with pop-up markers.

REWIND
For this deliverable, you’ve already done the following in this module:

Lesson 6.2.7: Add the weather data to a DataFrame
Lesson 6.2.7: Add the config.py file to the .gitignore file
Lesson 6.5.3: Create input statements
Lesson 6.5.3: Filter a DataFrame using the loc method
Lesson 6.5.4: Retrieve hotel data
Lesson 6.5.4: Add data to a pop-up marker
Lesson 6.5.4: Create a marker layer map
Create a folder called Vacation_Search.

Download the Vacation_Search_starter_code.ipynb file into your Vacation_Search folder, and rename it Vacation_Search.ipynb.

In the Vacation_Search.ipynb file, make sure the dependencies and API keys are imported correctly.

Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

In Step 1, import the WeatherPy_Database.csv file from your Weather_Database folder from Deliverable 1 as a DataFrame.

In Step 2, write two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation.

In Step 3, use the loc method to filter the city_data_df DataFrame for temperature criteria collected in Step 2, then create a new DataFrame.

In Steps 4a-b, determine if there are any empty rows, then drop them if necessary and create a new DataFrame.

In Steps 5a-b, use the provided code to create a new DataFrame, hotel_df, that will hold the hotel names from the hotel search in Steps 6a-6f.

In Step 6a, we have supplied the search parameters, which are the same as in this module, that you’ll need to use to search for a hotel for each city in Steps 6b-f.

In Steps 6b-f, iterate through the hotel_df DataFrame, retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters from Step 6a, then add the hotel name to the hotel_df DataFrame. If a hotel isn't found, skip to the next city.

In Step 7, drop any rows in the hotel_df DataFrame where a hotel name is not found.

Before exporting your DataFrame as a CSV, take a moment to confirm that your hotel_df DataFrame looks similar to the image below.
The new hotel DataFrame has the Hotel Name column completed where hotels are found.

In Steps 8a-b, create an output file to store the hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.

In Step 9, add the city name, the country code, the weather description, and the maximum temperature for the city to the info_box_template format template we have provided.

In Step 10a, use the provided list comprehension code to retrieve the city data from each row, which will then be added to the formatting template and saved in the hotel_info list.

In Step 10b, use the provided code snippet to retrieve the latitude and longitude from each row and store them in a new DataFrame.

In Steps 11a-b, refactor your previous marker layer map code to create a marker layer map that will have pop-up markers for each city on the map.

Take a screenshot of your map and save it to the Vacation_Search folder as WeatherPy_vacation_map.png.

The marker layer map with a pop-up marker for each city should look similar to the following image:
The new hotel DataFrame includes pop-up markers for each city.

Deliverable 2 Requirements
You will earn a perfect score for Deliverable 2 by completing all requirements below:

Input statements are written to prompt the customer for their minimum and maximum temperature preferences. (5 pt)
A new DataFrame is created based on the minimum and maximum temperature, and empty rows are dropped. (5 pt)
The hotel name is retrieved and added to the DataFrame, and the rows that don’t have a hotel name are dropped. (10 pt)
The DataFrame is exported as a CSV file into the Vacation_Search folder and is saved as WeatherPy_vacation.csv. (5 pt)
A marker layer map with pop-up markers for the cities in the vacation DataFrame is created, and it is uploaded as a PNG. Each marker has the following information: (5 pt)
Hotel name
City
Country
Current weather description with the maximum temperature
The marker layer map is saved and uploaded to the Vacation_Search folder as WeatherPy_vacation_map.png. (5 pt)
Be sure to double-check that you have the following in the Vacation_Search folder:

The Vacation_Search.ipynb file
The WeatherPy_vacation.csv file
The WeatherPy_vacation_map.png image

------------------------------------------------------------------------------------------------
Deliverable 3: Create a Travel Itinerary Map (40 points)
Deliverable 3 Instructions
Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.

REWIND
For this deliverable, you’ve already done the following in this module:

Lesson 6.5.4: Add data to a pop-up marker
Lesson 6.5.4: Create a marker layer map
Enable the "Directions API" in your Google account for your API key.

On the Google Cloud Platform, select "APIs & Services" from the left-hand side
Viewing the options on the Google Cloud Platform

Then, select "Library".
 Viewing the API Library on your Google Account

In the Search field, type "Directions".
 Viewing the API search field on your Google Account.

Select "Directions API".
Search for the Directions API in the search field on your Google Account.

Click "Enable" to activate the Directions API.
 Viewing the APIs on your Google Account.

Create a folder called Vacation_Itinerary.

Download the Vacation_Itinerary_starter_code.ipynb file into your Vacation_Itinerary folder and rename it Vacation_Itinerary.ipynb.

In the Vacation_Itinerary.ipynb file, make sure the dependencies and API keys are imported.

Use the instructions below to add code where indicated by the numbered-step comments in the starter code file.

In Step 1, import the WeatherPy_vacation.csv file from your Vacation_Search folder from Deliverable 2 as a DataFrame.

In Steps 2-4, copy or refactor the code from Steps 11a-b of Deliverable 2 to create a marker layer map of the vacation search results.

From the vacation search map, choose four cities that a customer might want to visit. They should be close together and in the same country.

You may have to refine your search with different weather criteria to get cities that are close together.
In Step 5, use the variables we have provided and the loc method to create separate DataFrames for each city on the travel route.

Hint: You will start and end the route in the same city, so the vacation_start and vacation_end DataFrames will be the same city.

In Step 6, use the to_numpy() function and list indexing to write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.
If you’d like a hint on using the to_numpy() function with list indexing, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

HINT
In Step 7, use the gmaps documentation (Links to an external site.) to create a directions layer map using the variables from Step 6, where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is either "DRIVING", "BICYCLING", or "WALKING".

Take a screenshot of your map from Step 7 and save it to the Vacation_Itinerary folder as WeatherPy_travel_map.png.

The directions layer map should look similar to the following image:
The directions layer for the vacation route.

In Step 8, use the provided concat() function code snippet to combine the four separate city DataFrames into one DataFrame.
If you’d like a hint on combining DataFrames into one DataFrame using the concat() function, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

HINT
In Steps 9-11, refactor the code from Steps 2-4 to create a new marker layer map of the cities on the travel route.

Take a screenshot of your map and save it to the Vacation_Itinerary folder as WeatherPy_travel_map_markers.png.

The marker layer map with a pop-up marker for each city should look similar to the following image:
The pop-up marker for each city for the vacation route.

Deliverable 3 Requirements
You will earn a perfect score for Deliverable 3 by completing all requirements below:

Four DataFrames are created, one for each city on the itinerary. (10 pt)
The latitude and longitude pairs for each of the four cities are retrieved. (5 pt)
A directions layer map between the cities and the travel map is created and uploaded as WeatherPy_travel_map.png. (10 pt)
A DataFrame that contains the four cities on the itinerary is created. (10 pt)
A marker layer map with a pop-up marker for the cities on the itinerary is created, and it is uploaded as WeatherPy_travel_map_markers.png. Each marker has the following information: (5 pt)
Hotel name
City
Country
Current weather description with the maximum temperature
Be sure to double-check that you have the following in the Vacation_Itinerary folder:

The Vacation_Itinerary.ipynb file
The WeatherPy_travel_map.png image
The WeatherPy_travel_map_markers.png image
Submission
Once you’re ready to submit, make sure to check your work against the rubric to ensure you are meeting the requirements for this Challenge one final time. It’s easy to overlook items when you’re in the zone!

As a reminder, the deliverables for this Challenge are as follows:

Deliverable 1: Retrieve Weather Data
Deliverable 2: Create a Customer Travel Destinations Map
Deliverable 3: Create a Travel Itinerary Map
Upload the following to your WeatherPy GitHub repository:

The Weather_Database folder with the following:

The Weather_Database.ipynb file
The WeatherPy_Database.csv file
The Vacation_Search folder with the following:

The Vacation_Search.ipynb file
The WeatherPy_vacation.csv file
The WeatherPy_vacation_map.png image
The Vacation_Itinerary folder with the following:

The Vacation_Itinerary.ipynb file
The WeatherPy_travel_map.png image
The WeatherPy_travel_map_markers.png image
A README.md that describes the purpose of the repository. Although there is no graded written analysis for this challenge, it is encouraged and good practice to add a brief description of your project.

IMPORTANT
Do not include your config.py file in your submission.

If you’d like a hint on how to not include the config.py file when adding your files to your GitHub repository, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

HINT
To submit your challenge assignment in Canvas, click Submit, then provide the URL of your WeatherPy GitHub repository for grading.

IMPORTANT
Once you receive feedback on your Challenge, make any suggested updates or adjustments to your work. Then, add this week’s Challenge to your professional portfolio.

NOTE
You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Submit then indicate you are skipping by typing “I choose to skip this assignment” in the text box.
