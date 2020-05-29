# App Structure

OrganicJS helps you organize your application code for better separation and ease of maintainance. It follows a `components` based approach where each component of your application resides in its own directory.

Suppose you are building your shiny new blog engine that has a `frontend` for displaying posts to your end users, and an easy to use `backend` for administration. Fire this command to scaffold you blog easily:

    $ organic gen-app frontend backend

It will scaffold your application with following structure:

    myApp
    |-- components
    |-- config
    |-- lib
    |-- middlewares
    |-- node-modules
    |-- public
    |-- services
    |-- index.js
    |-- package.json

If you expand the components folder, you should have two new folders named `frontend` and `backend`:

    myApp
    |-- components
        |-- frontend
        |-- |-- controllers
        |-- |-- models
        |-- |-- views
        |-- |-- middlewares.js
        |-- |-- routes.js
        |-- backend
        |--  |-- controllers
        |--  |-- models
        |--  |-- views
        |--  |-- middlewares.js
        |--  |-- routes.js

Thinking your `blog` application in terms of components like `frontend` and `backend` helps you split your code featurewise.