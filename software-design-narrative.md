# Software Design and Engineering Enhancement Narrative

## Artifact Description

The artifact I selected is my Travlr Getaways project from CS 465. It is a full-stack travel website built with Node.js, Express, Handlebars, MongoDB, and Mongoose. The original version used a JSON file to hold the trip information and display it on the travel page. I created the original project earlier in the Computer Science program and used it as the starting point for this enhancement.

## Why I Selected This Artifact

I selected this project because it includes a lot of different parts of software development in one place. It has routes, controllers, views, data, and a database connection that all have to work together.

I also picked it because the original project had areas that needed to be cleaned up and organized better. This made it a good project for showing that I can go back to older code, find problems, and improve the way it is designed instead of only creating something new.

## How I Improved the Artifact

The biggest improvement I made was moving the project away from only using a local JSON file and adding MongoDB and Mongoose.

I added a separate database connection file so the connection code was not mixed in with the rest of the application. I also added a Mongoose schema for the trip data. This gives the data more structure and helps stop incomplete records from being added.

I created a trips controller that gets records from MongoDB and returns them through the `/api/trips` route. I also added a seed script that loads the sample trips into the database.

Another improvement was better error handling. The original project was missing an error view, which caused problems when Express tried to display an error page. I added the missing error page and made the overall structure easier to understand.

## Course Outcomes

This enhancement helped me make progress toward the course outcome involving the use of tools and techniques to create useful computing solutions.

I used Node.js, Express, MongoDB, Mongoose, Handlebars, Git, GitHub, and MongoDB Compass together in one project.

It also helped me improve my software design skills because I had to decide how the database, model, controller, route, and views should work together.

## Reflection

The biggest thing I learned from this enhancement is that a project can work on the screen and still have problems with how it is built.

Moving the trip data into MongoDB helped me understand the full path from the database to the model, controller, route, and browser.

One challenge I had was that my first database seed failed because the schema required fields that were not in the original data. I had to compare the schema and the data and make them match.

I also had trouble with an older Mongoose shutdown method because the newer version no longer accepted the same callback. I fixed that by updating the code.

Overall, this enhancement helped me get better at organizing code, reading errors, fixing problems, and making an older project easier to maintain.
