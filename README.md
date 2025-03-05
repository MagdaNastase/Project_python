References:
Tkinter: https://docs.python.org/3/library/tkinter.html
Geopy: https://geopy.readthedocs.io/en/stable/
TimezoneFinder: https://pypi.org/project/timezonefinder/
OpenWeatherMap API: https://openweathermap.org/api
Installation:
To run the code, the following libraries are required: tk, geopy, timezonefinder, requests.
They can be installed using the command in CMD:
pip install tk geopy timezonefinder requests
Running the Code:
The code is executed using IDLE, by opening the file and selecting Run.

Functional Description + Backend:
The application provides a simple graphical interface with a search field for cities.

The user enters a city name and presses the Search button.
The city is geolocated using Geopy to obtain its coordinates and TimezoneFinder to determine its time zone.
The current local time of the city is displayed at the top of the window.
A request is made to the OpenWeatherMap API to fetch weather information for the specified city.
The weather data (temperature, condition, wind, humidity, and pressure) is displayed on the screen.
Function: getWeather
This function is triggered when the Search button is clicked.
It retrieves the city name entered in the input field (textfield) and uses Geopy to obtain its geographical coordinates (latitude and longitude).
Then, it utilizes TimezoneFinder to determine the time zone based on the given coordinates.
Using the time zone information, it fetches the current time in that location and updates the clock label.
Next, it constructs the API request URL for OpenWeatherMap using the city name, sends the request, and processes the JSON response to extract weather data.
The extracted weather information (temperature, condition, description, pressure, humidity, and wind speed) is then displayed in the corresponding labels (t, c, d, p, w, h).
Widgets (Labels, Entry, Button, etc.)
textfield: An input field where the user enters the city name.
myimage_icon: A search button with an icon, which triggers the getWeather function when clicked.
logo: A label displaying a logo image.
name, clock: Labels displaying the weather and current time.
label1, label2, label3, label4: Labels displaying wind speed, humidity, description, and pressure.
Notes
Images must be available in the current directory to ensure proper UI rendering.
An API key from OpenWeatherMap is required to fetch weather data and must be replaced in the code.
