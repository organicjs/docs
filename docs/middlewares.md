# Middlewares

OrganicJS suggests you to define middlewares at two levels: `application` level and`router` level.

## Application Level Middlewares

All your application level middlewares must be defined via`app.use` in the`middlewares/main.js` file.
This is the file that the framework loads while booting your application server.For ease of maintainence,
    you may define your middlewares in the`middlewares/definition` folder and refer to them in the`middlewares/main.js` file.

Below is an example for  application level middleware.

[filename](./snippets/middlewares1.md ':include :type=code javascript')

## Router Level Middlewares

These are middlewares specific to your current route.They are defined in the`middlewares.js` file per component.
Following is a sample authentication middleware for `ToDo App` tasks:

[filename](./snippets/middlewares2.md ':include :type=code javascript')
