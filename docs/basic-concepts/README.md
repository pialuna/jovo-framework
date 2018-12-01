# Basic Concepts

In this section, you will learn more about the essentials of building the logic of your Jovo Voice App.

* [Overview](#overview)
* [Handler](#handler)
* [Routing](#routing)
* [Data](#data)
* [Output](#output)

## Overview

![Alexa Skill Folder in a Jovo Project](../img/folder-structure-simple.png "Alexa Skill Folder in a Jovo Project" )

The `/app` folder contains all the logic necessary for your voice application. The `app.js` includes both a part about [App Configuration](../03_app-configuration './app-configuration'), as well as App Logic.

You can find out more about the basic concepts below.

## Handler

The `handler` is the main building block of your voice app. This is where the logic happens.

```javascript
app.setHandler({

    LAUNCH() {
        this.toIntent('HelloWorldIntent');
    },

    HelloWorldIntent() {
        this.tell('Hello World!');
    },
});
```

You can also define separate handlers for each platform to overwrite specific intents and states for platform specific app logic.

```javascript
app.setAlexaHandler({
    HelloWorldIntent() {
        this.tell('Hello Alexa user');
    }
});

app.setGoogleActionHandler({
    HelloWorldIntent() {
        this.tell('Hello Google user');
    }
});
```

## Routing

In section [App Logic > Routing](./01_routing './routing'), the concepts of intents and states are introduced, and how to route through them in the app's flow.


## Data

In section [App Logic > Data](./02_data, './data'), user input (slots and parameters) and user specific data are covered.


## Output

In section [App Logic > Output](./03_output './output'), you can learn more about how to craft speech, audio, and visual responses.


<!--[metadata]: {"description": "Find out how to build voice app logic with the Jovo Framework",
		        "route": "basic-concepts"}-->