# Plugins API

* [Introduction](#introduction)
* [Setup](#setup)
* [Start the server](#start-the-server)
* [Available REST API methods](#Available-REST-API-methods)
* [Examples](#examples)

## Introduction

This API groups together all the plugins available to users.
   
## Setup

* Start by cloning the project with git with `git clone https://mjollnir.unice.fr/bitbucket/scm/pee/private.git`
* Navigate to the source folder (by default `cd ./plugins`) and locate manage.py file. 

	### Windows

* If you want a virtual environment for your server, execute `python -m venv venv`. Then execute `venv\Scripts\activate`.
* Then Execute `pip install -r requirements.txt`.

	### Mac OS X and Linux

* If you want a virtual environment for your server, execute `python3 -m venv venv`. Then execute `source venv\bin\activate`.
* Then Execute `pip3 install -r requirements.txt`.

## Start the server

To start the server, execute `python manage.py runserver`.
You can change the ip or the port like this: `python manage.py runserver 127.0.0.1:8080`.
By default, python runs on [localhost:8000](http://localhost:8000).


## Available REST API methods


| HTTP METHOD           								| POST                  				| GET                   					| PUT                   			| DELETE                				|
| ----------------------------------------------------- | ------------------------------------- | ----------------------------------------- | --------------------------------- | ------------------------------------- |
| [/plugins](http://localhost:8000/plugins)            	| Error                 				| [List the Plugins](#list-the-plugins) 	| Error                 			| Error                 				|
| [/plugin](http://localhost:8000/plugin)              	| [Create a Plugin](#create-a-plugin) 	| [Search a Plugin](#search-a-plugin)   	| Error                 			| Error                 				|
| [/plugin/{id}](http://localhost:8000/plugin/0)       	| Error                 				| [Use a Plugin](#use-a-plugin)        		| [Edit a Plugin](#edit-a-Plugin) 	| [Delete a Plugin](#delete-a-plugin)	|


### List the Plugins

#### Request

    GET http://localhost:8000/plugins?format=json
    
#### Response
    
```json
{
    "result": {
        "plugins": [
            {
                "name": "Romanian Flag",
                "id": 0,
                "url": "http://localhost:8100/turing.machine/romanian-flag",
                "type": "enigma",
                "creation": "2018-01-13 03:14:15.926536",
                "last-edit": "2018-01-14 00:30:10.299956"
            },
            {
                "name": "Phone",
                "id": 1,
                "url": "http://localhost:8200/device/phone",
                "type": "device",
                "creation": "2018-01-14 00:30:10.299956",
                "last-edit": "2018-01-14 00:30:10.299956"
            },
            {
                "name": "LFA",
                "id": 2,
                "url": "http://localhost:8300/lfa",
                "type": "theme",
                "creation": "2018-01-01 23:14:06.926328",
                "last-edit": "2018-01-14 00:30:10.299956"
            }
        ]
    },
    "metadata": {
        "call": "GET http://localhost:8000/plugins?format=json",
        "date": "2018-01-14 03:32:19.280948",
        "version": 1
    }
}
```

### Search a Plugin

### Create a Plugin

### Use a Plugin

### Edit a Plugin

### Delete a Plugin


## Examples
