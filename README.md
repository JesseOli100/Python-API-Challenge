# Python-API-Challenge

# Background

Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

# Part 1: WeatherPy
In this deliverable, you'll create a Python script to visualize the weather of over 500 cities of varying distances from the equator. You'll use the citipy Python libraryLinks to an external site., the OpenWeatherMap APILinks to an external site., and your problem-solving skills to create a representative model of weather across cities.

For this part, you'll use the WeatherPy.ipynb Jupyter notebook provided in the starter code ZIP file. The starter code will guide you through the process of using your Python coding skills to develop a solution to address the required functionalities.

To get started, the code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

# Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude
To fulfill the first requirement, you'll use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

Latitude vs. Temperature

Latitude vs. Humidity

Latitude vs. Cloudiness

Latitude vs. Wind Speed

# Requirement 2: Compute Linear Regression for Each Relationship
To fulfill the second requirement, compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). You may find it helpful to define a function in order to create the linear regression plots.

Next, create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r values as you can see in the following image

![Snip20231128_3](https://github.com/JesseOli100/Python-API-Challenge/assets/62526904/b3800d15-549a-4801-a708-2b820311cebf)

You should create the following plots:

Northern Hemisphere: Temperature vs. Latitude

Southern Hemisphere: Temperature vs. Latitude

Northern Hemisphere: Humidity vs. Latitude

Southern Hemisphere: Humidity vs. Latitude

Northern Hemisphere: Cloudiness vs. Latitude

Southern Hemisphere: Cloudiness vs. Latitude

Northern Hemisphere: Wind Speed vs. Latitude

Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

# Part 2: VacationPy
In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the geoViews Python library, and the Geoapify API.

The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.

Your main tasks will be to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.

To succeed on this deliverable of the assignment, open the VacationPy.ipynb starter code and complete the following steps:

Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.

![Snip20231128_5](https://github.com/JesseOli100/Python-API-Challenge/assets/62526904/8877d9e9-7808-47dc-b1ab-56472c5cb3c6)

Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:

A max temperature lower than 27 degrees but higher than 21

Wind speed less than 4.5 m/s

Zero cloudiness

NOTE
Feel free to adjust your specifications but make sure to set a reasonable limit to the number of rows returned by your API requests.

Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.

For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

Add the hotel name and the country as additional information in the hover message for each city on the map as in the following image:

![Snip20231128_6](https://github.com/JesseOli100/Python-API-Challenge/assets/62526904/49f9f1e8-23ac-4a60-a101-0e16b58a1dc4)

# Hints and Considerations
The city data that you generate is based on random coordinates and different query times, so your outputs will not be an exact match to the provided starter notebook.

If you'd like a refresher on the geographic coordinate system, this siteLinks to an external site. has great information.

Take some time to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.

A starter code for citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by using the citipy Python libraryLinks to an external site.. Before you try to incorporate the library in your analysis, start with simple test cases outside of your main script to confirm that you are using it correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save you a lot of time and frustration.

You will need to apply your critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?

While building your script, pay attention to the cities you are using in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues.

Hint: Consider the full range of latitudes.
Once you have computed the linear regression for one relationship, you will follow a similar process for all other charts. Optionally, try to create a function that will create these charts based on different parameters. (Note: there will be no extra points for completing this.)

Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.

Ensure that your repository has regular commits and a thorough README.md file.

Lastly, remember that this is a challenging activity. Push yourself! If you complete this task, you can safely say that you've gained a strong understanding of the core foundations of data analytics, and it will only get better from here. Good luck!

# Sources

• Help from TA Matthew Werth and other staff

• Met up w/ other students during study groups to hash out the code through what we have learned so far

• Used StackOverFlow for issues on the code and/or to explain why certain pieces of the script were not running as intended

# Notes

What is the code supposed to be doing? What is the purpose of this exercise? 

The first point of this exercise is to make sure that we can integrate using our API Keys into a GitHub environment while hiding them at the same time. The second point of the exercise is to toggle with the dataframes to make sure that we are able to use the various Python libraries that are capable of generating various plots, maps, coordinates, etc. 

Syntax Learned:

•	%%capture – is used to capture the output of a cell and store it in a variable

•	--no-display – is specific to Jupyter Notebooks and is used to suppress the automatic display of the captured output 

•	!pip install cartopy – is used to install the Cartopy library using the pip package manager. Cartopy is a library for cartopgraphic projections and geospatial data visualization in Python. It is particularly useful for creating maps and working with geographical data.

•	!pip install geoviews – is used to install the GeoViews library using the pip package manager. GeoViews is an open-source Python library designed for easy creation and exploration of interactive geographical visualizations. 

•	!pip install pyproj – is used to install the pyproj library using the pip package manager. Pyproj is an interface PROJ library, which is used for performing cartographic projections and transformations. 

•	.iterrrows(): - is a method that returns an iterator yielding index and row data as pairs. It is used to iterate over the rows of a dataframe, providing access to both the index and the row data for each iteration.

•	.json() – It parses the content of an HTTP response that is in JSON format

- - -

This is submitted by Jesse Olivarez for the University of Utah: Data Analytics Bootcamp


