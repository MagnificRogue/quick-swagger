# Swagger

This repository provides a quick method by which swagger definitions for a given API may be defined or written. 

It accomplishes this by utilizing existing container definitions for Swagger: swagger-ui and swagger-editor. 

By default, running:

`$ docker-compose up` attaches the output of both containers to standard out, attaching them to localhost:8080 for the UI and localhost:8081 for the editor.

## Viewing

You can run `$ docker-compose up`, but if you always want it around you can always do:

`docker-compse up -d swagger-ui` which will create the UI in daemon mode.

You can see the state of this daemon using:

`$ docker-compose ps` 

If you need that port for something else, you can always kill it using:

`$ docker-compose kill swagger-ui`


## Editing

First, bring up the container for the editor using either `$ docker-compose up` or `$docker-compose up -d swagger-editor`.

Next, edit your changes in the fun UI. Lastly, you need to export the json edits that you've made and throw it in this repo to replace swagger.json
