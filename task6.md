# Discord Weather Bot
In this task you will be combing the two POCs from [task 2](https://github.com/IsAwesum/training-material/blob/main/task2.md) and [task 5](https://github.com/IsAwesum/training-material/blob/main/task5.md).


## Maven project
Create a Maven project and add dependencies for [JDA](https://github.com/DV8FromTheWorld/JDA) and [Unirest](http://kong.github.io/unirest-java/).

## Bot setup
Copy over the bot code from task 2 and ensure that the bot is able to connect and respond to commands.

## OpenWeatherMap REST client setup
Copy over the REST client and model code from task 5 into a class called `OpenWeatherMapService`.

A services is a concept in an application which is responsible for making calls to external (such a database or a REST API) or internal source (such as another service within the application) and returning back any data in the form of a model.

## !getWeather command
Add a `!getWeather` command to your Discord bot.

The command should return a message with the current details of the weather in London.

You will have to create a new instance of the OpenWeatherMapService object and then call the method which returns the model's data. Using this, send back a message with the weather info back to a user.

## !setCity command
Add a `!setCity [city name here]` command. You might need to [split](https://www.baeldung.com/string/split) the message to find the city name entered by the user.

Figure out a appropriate data structure to store a user's city. The user who sent the message can be identified using `getAuthor()` method on the `MessageReceivedEvent` object.

### Requirements for !setCity
* If the user has not set the city, then the `!getWeather` message should reply back with an appropriate message.
* If the user has set the city, then the `!getWeather` message should give back weather information for their chosen city.
* If the user uses `!setCity` again after already setting a city, then the new city should replace the saved city.

