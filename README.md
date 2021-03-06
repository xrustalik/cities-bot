# cities-bot
Telegram bot using Java Spring Boot.

# Bot usage

[Link to telegram bot](t.me/cities_admin_bot)

TOKEN=1243360459:AAEzMCyDYD6EbbXGJ1JyjLCzeQM44t336uA

After a `/start` command you'd see a message:

*Greeting, please type in City Name: I.e: Minsk*

# Running with Docker

To run this project inside Docker container you'd need to have Docker installed on your machine and run the following commands:

>`docker-compose up`

# Running locally

To run this project locally you'd need to have MySQL along with Java and Maven installed. Hibernate will automatically create and fulfill the database with needed information. You'd need to specify 
1. `spring.datasource.url`
2. `spring.datasource.username`
3. `spring.datasource.password` 

values in the **src/main/resources/application-local.properties** file. Those values are specific for you configuration. After all set up, please run the following commands:

>`mvn clean package`

>`java -jar -Dspring.profiles.active=local target/Bot-0.0.1.jar `  

# API 

We support these urls to use via REST request:

> POST: localhost:8080/api/city

  
>     "name":"New York",
>     "description": "Description"


> PUT: localhost:8080/api/city


>     "id":"5",
>     "name":"New York",
>     "description": "Description"

> DELETE: localhost:8080/api/city/{name}

> GET: localhost:8080/api/city/{name}