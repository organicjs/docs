# Defining Routes

All the routes you define follow a structure described as:

    'method path': 'Controller.action'

See few examples below for reference:

[filename](./snippets/routes.md ':include :type=code javascript')

Note that the `controller` must match the controller's file name and all your http `methods` must be in lowercase.

## Complex Routes

In case you need more control of your routes, you may do so in the `middlewares.js` file of your component.