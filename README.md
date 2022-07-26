# World Weather Analysis (using Python & Google APIs)

## Project Overview
Our client is PlanMyTrip, a company that provides web-based services to help clients plan their travel and to select & book hotels. In the current project, we have been asked to use Python methods and modules, together with Google APIs, to determine and plot the relationship between latitude and a variety of weather parameters. The client has requested two main deliverables:

	<ol>
	<li> Deliverable #1 = Retrieve weather data (--> generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with Google's OpenWeatherMap); and
	<li> Deliverable #2 = Create a customer travel destinations map (--> use python input statements to retrieve customer weather preferences, identify potential travel destinations and nearby hotels given these data, and create a marker layer map with pop-up markers for each city); and
    Deliverable #3 = Create a travel itinerary map (--> use python input statements to retrieve customer weather preferences, identify potential travel destinations and nearby hotels given these data, and create a marker layer map with pop-up markers for each city);
	</ol>

PlanMyTrip will use these deliverables to collect and present real-time data for end users via a search page, which users can filter based on preferred dates of travel and preferred weather conditions. Results will help users decide when (what time of year) and where (e.g., cities in Northern vs. Southern Hemisphere) to book  reservations.

## Resources (Software & Web-based resources)
For this project, we have used the following software and web-based resources:
	<ol>
	<li> Jupyter Notebooks & Python 3, together with the following modules:
    	<ol>
        <li> Pandas
        <li> CityPy
        <li> SciPy
        <li> Matplotlib
        </ol>
	<li> Google APIs, including the following web-based methods and resources:
        <ol>
        <li> JSON traversals
        <li> OpenWeatherMap
        <li> Jupyter G-Maps 
        <li> Google Places API
        </ol>
	</ol>

## Methods and Resources
We used the above methods and resources to carry out the following specific tasks:  
	<ol>
	<li> Retrieved cities for >500 representative (world-wide) latitudes & longitudes (Resources & Methods: Python (Jupyter Notebooks) > CityPy Module);
	<li> Retrieved weather data for each of the cities (Resources & Methods: JSON traversals, Google Weather Maps API);
	<li> Created a DataFrame to store the data (Resources & Methods: Python > Pandas Library);
	<li> Created scatterplots that show the relationship between latitude & weather parameters for the cities of interest (Resources & Methods: Python > Matplotlib Module) 
	<li> Performed linear regression on data from Northern & Southern hemispheres (Resources & Methods: Python > SciPy Module);
	<li> Mapped the cities and created visualization (heatmaps) (Resources & Methods: Jupyter G-Maps & Google Places API).
	</ol>

## Results
Deliverables for this project are stored in the following directory and file structure:
	<ol>
	<li> A Weather_Database directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Weather_Database), which contains the following files:
    	<ol>
	    <li> Weather_Database.ipynb
        <li> WeatherPy_Database.csv
        </ol>
	<li> A Vacation_Search directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Vacation_Search), which contains the following files:
        	<ol>
	    <li> Vacation_Search.ipynb
        <li> WeatherPy_vacation.csv
        <li> WeatherPy_vacation_map.png
        </ol>
	<li> A Vacation_Itinerary directory (https://github.com/gwenfrishkoff/World_Weather_Analysis/tree/main/Vacation_Itinerary), which contains the following files:
        	<ol>
	    <li> Vacation_Itinerary.ipynb
        <li> WeatherPy_travel_map.png
        <li> WeatherPy_travel_map_markers.png
        </ol>
	</ol>
