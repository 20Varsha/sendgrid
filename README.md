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
## Creating an Object 
``` const obj = {
    subject: "SendGrid Email Template",
    heading: "Welcome to SendGrid Email template",
        description:"Hi Sooraj, Thank you for your interest in SendGrid Please confirm your Mail"
  
    button: "Confirm",
    acknowledgment: "Regards,",
    name: "Varsha P M",
};
```
## Steps -9
## Create an HTML Template

``` 
let htmlTemplate =`
 <!DOCTYPE html>
 <html>
 <body>
 <h1>${object.heading}</h1>

 <button style="background-color: #4CAF50;
 border: none;
 color: white;
 padding: 15px 32px;
 text-align: center;
 text-decoration: none;
 display: inline-block;
 font-size: 16px;
">
${object.Button}</button>
<p>${obj.acknowledgment}</p>
<p>${obj.name}</p>

 </body>
 </html>
 `;  
 ```

## Steps -10
## Create http request using Axios
``` const callMethod = () => {
    axios({
        method: "post",
        url: "https://api.sendgrid.com/v3/mail/send",
        headers: {
            Authorization:
               `Bearer ${send_Api}`
        },
        data: {
            personalizations: [
                {
                    to: [
                        {
                            email:"varshapm313@gmail.com",
                            name:""                        },
                        {
                            email:"varshapm313@gmail.com",
                            name: "Varsha"

                        },

                    ],
                    subject: `${object.subject}`
                }
            ],
            from: {
                email: "varsha.monachan@urolime.com",
                name: "varsha"
            },
            content: [{ type: "text/html", value: htmlTemplate }]
        }
    });
};

callMethod(); 
```

## Step-11
## Run the Project
###### Send message using SengGrid.Use the command for Run the project 
``` node service.js ```




