# SendGrid Html Email Template
## Descrition
###### Sending mail template through SendGrid using Node Js
## Software name and Version
###### Node.js v16.14.0
## Installation
###### Install Node.js
## Steps-1
###### Create SendGrid Account
###### Signup in the sendgrid
###### Authenticate Sender email address to verify and confirm
###### Create an API key 
## Step-2
###### Create New project in Node Js
###### Create a new Node.js project using the command
``` npm install ```
## Steps -3
## Install Axios dependency
Axios is a Javascript library used to make HTTP requests from node 
js or XMLHttpRequests from the browser and it supports the Promise API 
that is native to JS ES6. It can be used intercept HTTP requests and 
responses and enables client-side protection against XSRF.
###### Install the Axios dependency using the command
``` npm install axios ```
## Steps -4
## Install the dependencies for Environment Variable
###### Environment Variable is used to store the API Key. Install dependency for Environment Variable  using the command
``` npm install dotenv ```
## Steps -5
## Create a .env file in the folder and set the sendgrid api.
``` Send=*********API-key****************** ```
## Steps -6
## Import all the dependencies to the file service.js
``` const axios = require('axios');const dotenv = require("dotenv") ```
## Steps -7
## Set the API key
###### API key stored by the environment variable
``` const sendGridAPIKey = process.env.Send ```
## Steps -8



