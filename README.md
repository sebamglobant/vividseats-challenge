# Interview challenge

# Challenge

Welcome!

Thanks for taking our coding challenge! We'd like for you to implement a basic event management system, from frontend to backend.

The features we'd like to develop are:

* Display events (event name, date, venue name, city, state) in a table
* Add events

Feel free to take creative liberties: you may use any open source frameworks or libraries you like.

We provided you with some HTML (index.html) to start as well as some Spring boilerplate for a backend server, but you are welcome to change this.

We also provided you with our 'event-service.js'. This file should be modified to interact with the backend server you develop.

Unit tests are optional.

Steps to complete:
1) Create a Venue table to match the schema defined by Venue.java
2) Modify the events table to contain a venueId column
3) Create a venue when the app starts - Wrigley Field - and make sure that venue is linked to the White Sox vs. Cubs event
4) Modify the events API to populate the Venue data when querying out a list of events
5) Create an insert event API
6) Implement JavaScript functions to fetch event data and insert a new event
7) Use your new REST API + JavaScript functions to build frontend of app

The frontend of the app should show the list of events in the database on page load and then dynamically update when a new event is added.

Extra credit:
1) Migrate the JS to use ES6 along with a modern framework and build system (i.e. React or Angular with webpack)
2) Dockerize the application

On any system with the JDK installed, running the application from the command line should be as simple as './gradlew bootRun'. You may want to leverage an IDE to develop and debug. The application will be available on localhost:8080.

Best of luck!

# how it works
This project in build with gradle, so you can run in the project's root folder: 

```
./gradlew bootRun
```

this command will build all the frontend project (Angular) and serve it in `localhost:8080` with the API under the same url.

## using docker
To run the app in a docker container you have to run the following commands on the project's root folder

1. Generate the .jar file
``` ./gradlew bootJar ```
2. Create the docker image
``` sudo docker build -f ./docker/Dockerfile -t interviewapp:lastest . ```
3. Run the container
``` sudo docker run -d -p 8080:8080 --name interview-container  interviewapp ```

if docker is unable to find image 'interviewapp:latest' locally, run the command again with the image ID instead of `interviewapp` 