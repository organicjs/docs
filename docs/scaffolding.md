# Scaffolding

OrganicJS helps you auto-generate your new project's files and folder easily. But before going further, you will have to understand two terms used by OrganicJS: `project` and `component`

Let us suppose you have decided to roll out your own shiny new blog engine by the name `rabbit-blog` and for ease of maintainence amd modularity, you decided to separate the `client` and `admin` code by keeping them in their own folders.

Let us summarize it this way:

    Project: rabbit-blog
    Components: client & admin
    Route '/': client
    Route '/admin-panel': admin

## Generating Project

In you terminal, running following command will scaffold your project:

    $ organic-cli app rabbit-blog

The above command generate a number of files and folders in your current durectory. Now you must install all the project dependencies declared in the `package.json` file by default.

    $ npm install

If so far things are working fine, you have successfully created your new project.

## Generating Components

Now you need to move into your newly generated project directory:

    $ cd rabbit-blog

To create the `client` component, type following:

    $ organic-cli component client

You should now see that a folder named `client` has been created in the `components` folder. Repeat the same for `admin` component.

## Configuring Routes

We have decided that all the requests made with route prefix `'/'` must be served by the `client` component. Similarly, requests made with route prefix `'/admin-panel'` must be served by the `admin` component.

For this, move into the `config` folder of your project root, i.e. the `rabbit-blog` folder.

There you will find three configuration files named `development.json`, `production.json`, and `test.json`. By default, the configuration settings are read from the `development.json` file.

Open the `development.json` file and configure the `components` key with following:

    components: {
        '/': 'client',
        '/admin-panel': 'admin'
    }

## Running Your App

Run the following command from your projerct root:

    $ node index.js

It should start you app on default `port:3000`

    http://localhost:3000
