# Python API Challenge

Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

## Before You Begin

1. Create a new repository for this project called `python-api-challenge`. Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, create a directory for this assignment. Use a folder name that corresponds to the Challenges, such as `WeatherPy`.
4. Inside the folder you just created, add the files called `api_keys.py`, `WeatherPy.ipynb`, and `VacationPy.ipynb` that you will find in the starter code ZIP file provided. These will be the main scripts to run for each analysis.
5. Before you push your changes to GitHub, add a `.gitignore` file.

#### Add a `.gitignore` File

For this assignment, you will need to add a `.gitignore` file to your repo. Doing so will prevent the `api_keys.py` file that contains your API key from being shared with the public. If you skip this step, anyone using GitHub could copy and use your API key, and you may incur charges as a result.

To get started, type `git status` in the command line to see a list of all the untracked files that you have created so far.

To add only the `WeatherPy.ipynb` file to GitHub, for example, type `git add WeatherPy.ipynb`. Keep in mind that you would have to add each file individually when adding or updating a file. A more efficient solution is to add all of the files that you don't want to track to the `.gitignore` file.

Before adding your files to GitHub, add `api_keys.py` to the `.gitignore` file by following these steps:

1. Open your `python-api-challenge` GitHub folder in VS Code.
2. Open the `.gitignore` file and type the following code on the first line:

#Adding config.py file.
api_keys.py

4. 3. In the command line, type `git status` and press Enter. The output should indicate that the `.gitignore` file has been modified and the `api_keys.py` file is untracked.
5. Use `git add`, `git commit`, and `git push` to commit the modifications to the `.gitignore`, `WeatherPy.ipynb`, and `VacationPy.ipynb` files to GitHub.
6. On GitHub, the only new python files you should find are `WeatherPy.ipynb` and `VacationPy.ipynb`.



## Instructions

This activity is broken down into two deliverables, WeatherPy and VacationPy.

### Part 1: WeatherPy

In this deliverable, you'll create a Python script to visualize the weather of over 500 cities of varying distances from the equator. You'll use the `citipy` Python library, the OpenWeatherMap API, and your problem-solving skills to create a representative model of weather across cities.

For this part, you'll use the `WeatherPy.ipynb` Jupyter notebook provided in the starter code ZIP file. The starter code will guide you through the process of using your Python coding skills to develop a solution to address the required functionalities.

**Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude**

To fulfill the first requirement, you'll use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

- Latitude vs. Temperature
- Latitude vs. Humidity
- Latitude vs. Cloudiness
- Latitude vs. Wind Speed

**Requirement 2: Compute Linear Regression for Each Relationship**

To fulfill the second requirement, compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). You may find it helpful to define a function in order to create the linear regression plots.

Next, create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r values as you can see in the following image:

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/MaxTemp(Fig1).png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/(Humidity)Fig2.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/Cloudiness(Fig3).png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/WindSpeed(Fig4).png)


You should create the following plots:

- Northern Hemisphere: Temperature vs. Latitude
- Southern Hemisphere: Temperature vs. Latitude
- Northern Hemisphere: Humidity vs. Latitude
- Southern Hemisphere: Humidity vs. Latitude
- Northern Hemisphere: Cloudiness vs. Latitude
- Southern Hemisphere: Cloudiness vs. Latitude
- Northern Hemisphere: Wind Speed vs. Latitude
- Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

### Temperature vs. Latitude Linear Regression Plot
***

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%205%20Northern%20Hemi.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/Fig%206%20Southern%20Hemi.png)

#### Discussion about the linear relationship:

The R squared value for the Northn Hemisphere data was 0.60 and the R squarred for the Southern Hemisphere was 0.61. Both models had a moderate amount of variance with the Northern Hemisphere showing slightly higher varience. This makes perfect sense as there are many factors besides latitude that would affect the temperature of any location. Some examples would include approximate distance from water bodies, altitude, presence of wind, cloudiness or weather.

From the equation of the line we can see that the slope is positive for the Southern Hemisphere as it approaches the equator (0) and negative in the Northern Hemisphere as it approaches the Equator. Both of these slopes make complete sense because the temperature as one moves from the poles into the equator will be warmer.

Also, the larger slope in the Southern Hemisphere indicates a quicker change in temperature as one approaches the equator but it does not reach as high of a maximum temperature (25-35C) as it reaches the equator, whereas the Northern Hemisphere warms up at a slower rate but sees a higher maximum temperatures closer to the equator (30-40C).


### Humidity vs. Latitude Linear Regression Plot
***

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%207%20northern.png)


![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%208%20Southern.png)

#### Discussion about the linear relationship:

The linear regression results and the slope for both the Northern and Southern Hemispheres indicated that there was too much variation in the data to show any correlation between the latitude and humidity. The slow for both indicated a slight slope that is almost not present. In the case of the Southern Hemisphere it increased at a slper of 0.02 towards the equator but in the case of the Northern Hemisphere, the slope increased as the distance moved away from the equator.

Although further analysis of data would need to be carried out, based on this data alone, there are too many factors that affect the humidity of an area to say it is just based on latitude alone.

### Cloudiness vs. Latitude Linear Regression Plot
***

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%209%20northern.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%2010%20Southern.png)

#### Discussion about the linear relationship:

The cloudiness in the Nothern Hemisphere appears to have a relatively low R squared value. As can be observed form the data and the line of regression (slope = 0.02) the relationship between Cloudiness and Latitude has a lot of variation coming from other factors.

In the Southern Hemisphere the data indicates a slight increase (slope =0.36) in cloudiness as the Latitude approaches the equator. The R squared is relatively low indicating there is a large amount of variation that is likely caused by other sources.

### Wind Speed vs. Latitude Linear Regression Plot
***
![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%2011%20Northern.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/fig%2012%20southern.png)

#### Discussion about the linear relationship:

The variation in the wind speed results for each lattitude in the Northern Hemisphere resulted in an R squared of 0.0002. The consistency in the wind speeds at all lattitudes is quite impressive.

In the Southern Hemisphere the R squared (0.030) also indicated that variation at each lattitude was high. There was a very slight decrease in Wind Speed as the results approached the equator (0).

Interestingly, the wind speed in the Northern Hemisphere concentrated between 0 and 10 m/s (with some values outside of this range of course, where as the winds in the Southern Hemisphere were concentrated between 0-7 (m/s).

It would be interested to determine if there were significant differences in the data sets.

***
## Part 2: VacationPy

In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the `geoViews` Python library, and the Geoapify API.

The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.

Your main tasks will be to use the Geoapify API and the `geoViews` Python library and employ your Python skills to create map visualizations.

To succeed on this deliverable of the assignment, open the `VacationPy.ipynb` starter code and complete the following steps:

1. Create a map that displays a point for every city in the `city_data_df` DataFrame as shown in the following image. The size of the point should be the humidity in each city.


![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/step%201%20map.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/Step%201%20Map%20Hover.png)

2. Narrow down the `city_data_df` DataFrame to find your ideal weather condition. For example:

- A max temperature lower than 27 degrees but higher than 21
- Wind speed less than 4.5 m/s
- Zero cloudiness

**NOTE**: Feel free to adjust your specifications but make sure to set a reasonable limit to the number of rows returned by your API requests.

3. Create a new DataFrame called `hotel_df` to store the city, country, coordinates, and humidity.

4. For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

5. Add the hotel name and the country as additional information in the hover message for each city on the map as in the following image:

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/Step%205%20map.png)

![](https://github.com/TraceyGeneau/python-api-challenge/blob/main/output_data/Step%205%20Map%20Hover.png)



 

 
