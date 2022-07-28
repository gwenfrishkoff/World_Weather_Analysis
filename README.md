# World Weather Analysis (using Python & Google APIs)

## Project Overview
Our client is PlanMyTrip, a company that provides web-based services to help clients plan their travel and select & book hotel reservations. For the current project, we have been asked to use Python methods and modules, together with OpenWeatherMap and Google APIs, to determine and plot the relationship between latitude and a variety of weather parameters and to collect end user data to generate travel itineraries and maps. 

The client has asked us to write python code that produces three deliverables:

	<ol>
	<li> Deliverable #1: Generate GCS coordinates and retrieve weather data for nearby cities; 
	<li> Deliverable #2: Create a user-driven travel destinations map; and
	<li> Deliverable #3: Create a travel itinerary map that corresponds to user preferences.
	</ol>

PlanMyTrip will use these deliverables to collect and present real-time data for end users via a search page, which users can filter based on preferred dates of travel and preferred weather conditions. Results will help users decide when (what time of year) and where to book reservations. 

## Resources (Software & Web-based resources)
For this project, we used the following software and web-based resources:
	<ol>
	<li> Jupyter Notebooks & Python 3, plus the following dependencies (imported modules):
    	<ol>
		<li> NumPy (Deliverable #1)
        <li> CityPy (Deliverable #1)
		<li> Requests (Deliverable #2)
        <li> Matplotlib (Deliverable #2)
		<li> SciPy (Deliverable #3)
        </ol>
	<li> Google APIs, including the following web-based methods and resources:
        <ol>
        <li> OpenWeatherMap (Deliverable #1)
        <li> Jupyter G-Maps (Deliverable #2)
        <li> Google Maps, Places, & Directions APIs (Deliverable #3)
        </ol>
	</ol>

## Overview: Methods and Resources
We used the above methods and resources to carry out the following specific tasks:  
	<ol>
	<li> Generated 2,000 random latitudes & longitudes (Resources & Methods: Python > NumPy Module);
	<li> Retrieved cities for each combination (i.e., pair) of latitudes & longitudes (Resources & Methods: Python > CityPy Module);
	<li> Retrieved weather data for each of the cities (Resources & Methods: Python > Requests module (for JSON traversals) & OpenWeatherMap API);
	<li> Created DataFrames to store the data (Resources & Methods: Python > Pandas Library);
	<li> Created scatterplots that show the relationship between latitude & weather parameters for the cities of interest (Resources & Methods: Python > Matplotlib Module) 
	<li> Performed linear regression on data from Northern & Southern hemispheres (Resources & Methods: Python > SciPy Module);
	<li> Mapped the cities (Resources & Methods: Jupyter G-Maps).
	<li> Created heatmaps to visualize regression results (Resources & Methods: Google Places API).
	</ol>

## Methods (Deliverable #1): Retrieving Weather Data
For Deliverable #1, we wrote python code that generates a set of GCS data (latitude-longitude coordinate pairs), retrieves a list of nearby cities, and performs web-based (API) calls to retrieve weather data for each city.

We used *NumPy* to generate a set of 2,000 random latitude-longitude coordinate pairs and *CitiPy* to retrieve a list of nearest cities for each coordinate pair.  We then used *OpenWeatherMap* to perform an API call to retrieve the following weather data for each city:
	<ol>
	<li> City & country
	<li> Date
	<li> Latitude and longitude
	<li> Maximum temperature
	<li> Humidity
	<li> Cloudiness
	<li> Wind speed

After we retrieved the data, we used *Pandas* to add them to a DataFrame and exported the tabular results to .csv files. 

The python code to create this deliverable is stored in the file 'Weather_Database.ipynb', and the exported data are saved to the file 'WeatherPy_Database.csv'.

## Methods (Deliverable #2): Create Customer Travel Destinations Map
For Deliverable #2, we wrote a python script that filters data based on user preferences (preferred weather conditions) and identifies potential travel destinations and nearby hotels. We used Python *Requests* to create the Input statements that prompt end users for their weather preferences.  

We then used *Matplotlib* to create a marker layer map with pop-up markers for the cities of interest, to show the relationship between latitude & weather parameters for each city.

The python code to create this deliverable is saved to the file 'Vacation_Search.ipynb'. The exported data are saved to the file 'WeatherPy_vacation.csv', and the marker layer map is saved to the file 'WeatherPy_vacation_map.png'.

## Methods (Deliverable #3): Performing Linear Regression ()
For Deliverable #3, we wrote a script that selects four cities from the list of potential travel destinations, creates a travel itinerary, and produces a marker layer map to visualize the results. 

Gmaps *Direction Service* (https://jupyter-gmaps.readthedocs.io/en/latest/tutorial.html#directions-layer) was used to create the directions layer map.The map has been saved to the file 'uploaded as 'WeatherPy_travel_map.png', and marker layer map of the cities along the travel routes and saved it to the file 'WeatherPy_travel_map_markers.png'. 

## Results
The three sets of deliverables for this project are stored in the following Github directories:
	<ol>
	<li> Weather_Database directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Weather_Database), which contains the following files:
    	<ol>
	    <li> Weather_Database.ipynb
        <li> WeatherPy_Database.csv
        </ol>
	<li> Vacation_Search directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Vacation_Search), which contains the following files:
        	<ol>
	    <li> Vacation_Search.ipynb
        <li> WeatherPy_vacation.csv
        <li> WeatherPy_vacation_map.png
        </ol>
	<li> Vacation_Itinerary directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Vacation_Itinerary), which contains the following files:
        	<ol>
	    <li> Vacation_Itinerary.ipynb
        <li> WeatherPy_travel_map.png
        <li> WeatherPy_travel_map_markers.png
        </ol>
	</ol>

*Note*: The config.py file, which stores the API keys, is not uploaded to the GitHub repository (it has been added to the .gitignore file to pre-empt upload).