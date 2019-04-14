# JS401 - Lab-20 Cloud Deployment
## Author: Cory Henderson
This lab deploys the files from lab 19 onto AWS, Azure, and Heroku in order to demonstrate cross cloud platform interaction.

## Links and Resources
- [Q-Server Github](https://github.com/401-advanced-javascript-1/lab-19-QServer/tree/submission)
- [Q-Server AWS](http://qserver-env.m9cxwupgsr.us-west-2.elasticbeanstalk.com/)
- [Q-Logger Github](https://github.com/401-advanced-javascript-1/lab-19-logger/tree/working)
- [Q-Logger Azure](https://q-logger-cory.azurewebsites.net/)
- [API Github](https://github.com/401-advanced-javascript-1/lab-19-api-server/tree/working2)
- [API Heroku](https://shielded-harbor-73029.herokuapp.com/)
- [Travis](https://www.travis-ci.com/401-advanced-javascript-1/lab-13-bearerAuth)

# Modules
- app.js: contains functionality for read/update/write files
- server.js: opens port and contains handler functions for socket events
- logger.js: contains socket event listeners which log save/error events
- API:
 - app.js: sets up application
 - v1.js: sets routes and route handlers

# Setup
Using the above listed AWS server link, set "Q-SERVER=(AWS LINK)" in your .env file for the logger.js and API applications. This will point the Q-clients to subscribe to the AWS server. When requests are made to the API, it will know to emit to the AWS server, and the logger at  will know where to listen and log events.

To post to the Heroku API server, use postman, and include the required schema fields in the request body.

## Tests
- Testing for expected route endpoints was performed using Postman and following the required schemas for teams and players.
