# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

## MVP

### Task
![Diagram showing the dataflow](https://github.com/krismac/CodeClan_w08d01_hw_full_stack_preparation/blob/master/Screenshot%202018-10-30%20at%2009.30.28.png) 


### Questions

Questions
1. What is responsible for defining the routes of the games resource?
- Get(), post() and delete() methods are defined in the Request file.

2. What are the the responsibilities of server.js?
- The modules that must be imported for managing the apps interaction of express and the MongoClient are defined. The static path of public files, configuration of express and the database connection is established in server.js.

3. What are the responsibilities of the gamesRouter?
- A router is a function for defining the servers (server.js) routing methods (get, post, delete and put) should be called. The gamesRouter is an instance of this function specifically for the 'games' element of the app receives/responds on behalf of the object. 

4. What process does the the client (front-end) use to communicate with the server?
- The client uses http GET, POST, DELETE and PUT methods to communicate to the server

5. What optional second argument does the `fetch` method take? And what is it used for in this application? 
- The fetch() method can accept a second parameter (init object). This can allow us to controll a number of settings within the method implementation e.g. POST inc mode, cache, credentials, headers, redirects, referrals and predefining a response action. 

- Within the requesthelper, it supports with defining how the post handles the JSON payload. 

6. Which of the games API routes does the front-end application consume (i.e. make requests to)?
- GET - '/', 
- POST - '/', 
- DELETE - /:id

7. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
- An interface between the server-side javascript code and the MongoDB database application

## Extension
8. Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
- These sequential and unique identifiers are appended automatically by MongoDB to each record thereby allowing us to specify a record for retrieval, update or to deletion.
