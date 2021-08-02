# Task 4 -  Discord Weather Bot Prep.

In this task you will be doing the prep. work for building a Discord weather bot. 

Your bot will allow a user to set their city with a `!setCity [city name here]` command and then get a weather report using `!getWeather` command which will show the current weather for their city.


## API
In order to retrieve weather data for a user, your bot will need to communicate with an API.

An API is a way to integrate your application with another application. In this case, you will be using the [OpenWeatherMap](https://openweathermap.org/) API which will provide weather data to integrate with your bot.

Similarly, your bot communicates with the Discord API to listen and respond to messages a Discord user sends. 

APIs are a powerful concept which you can use to build an application - they are available for most things you can think of. From providing [Fruit related data](https://www.fruityvice.com/) to [Valorant skins/maps/game mode data](https://developer.riotgames.com/apis#val-content-v1/GET_getContent).

This [short video](https://www.youtube.com/watch?v=s7wmiS2mSXY) is a good overview on the concept of APIs.

## OpenWeatherMap API
The OpenWeatherMap API is a REST based API which means you communicate to it using HTTP "endpoints" - "endpoint" is just a fancy word for a url. 

HTTP endpoints accept different methods such as "GET", "POST", "PUT" and "DELETE". 

Since you want to _retrieve_ weather data you will be using the "GET" method (which is the default method when a browser hits an URL).

### Current weather data endpoint
The OpenWeatherMap API provides an endpoint which you will use to find the current weather data for a city:
https://openweathermap.org/current

Try out the city endpoint url in your browser, replacing `{city name}` with a city name of your choice. See what the result is.

#### API Key
You should have noticed an error mentioning an invalid API key.

API keys are used by some APIs to protect data as to only allow people with a key to access data.

Sign up for an API key and then wait for 15 mins. 

After 15 mins, revist the url but this time replace `{API key}` with the API key provided. 

You should now see some meaningful data in a JSON format. JSON is an important but easy-to-understand concept, watch [this short video](https://www.youtube.com/watch?v=sSL2to7Jg5g) for a good explanation. 
