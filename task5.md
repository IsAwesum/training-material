# Weather retrieval POC

In this task you will be creating a weather retrieval POC which you will use to create your Discord bot.

## Maven project

Create a Maven project in IntelliJ.

## Creating the model

Within an application, an object that is used to represent data is known as a model. 

Visit the endpoint you used to retrieve the weather data from OpenWeatherMap. 
You will be representing the JSON returned at this endpoint in your object. 
The JSON fields you see need to be represented as object attributes in your class, the variable names need to match the JSON fields exactly.


For example, for the following JSON:

```
{
    "id": 4,
    "description": "This is an example",
    "ratings": [
        {
            "positive": 12,
            "negative": 4
        }
    ]
}
```

The model object would look like the following:

```
import java.util.List;

public class Data {
    private int id;
    private String description;
    private List<Rating> ratings;
}
```
```
public class Rating {
    private int positive;
    private int negative;
}
```

For the purposes of this POC pick only the `weather`, `visibility` and `name` JSON elements to represent in your object.

## Using Lombok for getters/setters
Getters and setters are required for your class to automatically convert JSON to objects.

[Lombok](https://projectlombok.org/) is a library which provides various code generation utilities to help save you from writing code. Include Lombok in your maven dependencies.

One of these code generation utilities provided by Lombok is automatic generation of getters and setters through the `@Getter` and `@Setter` annotation.

Add [these annotations](https://kodejava.org/how-do-i-generate-getters-and-setters-with-lombok/) to your classes.


## Unirest REST client
The API provided by OpenWeatherMap is known as a REST API. 

A REST API has certain characteristics:
* Communication is done using the HTTP(S) protocol using methods (such as GET, POST, PUT etc)
* Endpoints (URLs) are used to interact with particular parts of the API

To communicate with a REST API in Java we need to use a REST client. Your browser is technically a REST client and is cabable of sending GET, POST, PUT requests to an endpoint.

### Unirest dependency
Add the [Unirest dependency](http://kong.github.io/unirest-java/) to your project

### Constructing a request with Unirest
We will be using a technique called mapping to convert JSON at the endpoint to an Object. A good example of the mapping functionality provided by 
Unirest [can be found in the docs](http://kong.github.io/unirest-java/#responses)

Create a GET request to your endpoint using Unirest and put the code into a `main` method. You can then debug that piece of code to see if the mapping has worked correctly. 

