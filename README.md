# python-flask-app-on-heroku

This is a template for putting hosting a python flask app with heroku. Each significant file is explained below.

## Procfile
Lists the processes for heroku to spin up dynos for. This app uses gunicorn for web processes, and gunicorn uses the 'app' from the wsgi file. 
This is all under one command 'web'.

## requirements.txt
Lists the package requirements for the app. At minimum, the following must be listed: gunicorn, flask. It is **critical** to note that heroku 
requires this file to build the python app. It will fail to build unless this file exists (even if its empty)

## runtime.txt
States the pyton version to be used.

## wsgi.py
Imports the flask app from app/main.py and runs it. Is also called by the web process dyno on heroku.

## main.py
Initializes the flask app. Holds all of the routes for the app and which python functions to run when.

