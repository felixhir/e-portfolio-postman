# E-Portfolio: Postman - How to build and automate API-tests

## Structure
You will find the slides shown during the presentation in 'presentation/index.html'.
The API-definition and created collection + environment are found in the 'postman/'-
directory.

## Getting started
Create an account in order to use the collections via the Postman-API or just get the desktop application.
Both options are available [here](https://www.postman.com/).
<br>
In order to test an API you need to create a collection manually or import an (Open-)API-definition 
(the demo is 'postman/rubber-ducks.json). The collection should contain requests to the resources
you plan on testing.
<br>
In case of working with a mock-server create one under the respective menu and don't forget to add
example responses to your requests under the '...' option next to them. Otherwise you will expect your APIs
responses, of course.

## Writing Tests
To test your API simply go to the requests and add the tests you want to execute in the 'Tests'-submenu.
You can either create your own or use the snippets. The tests are done in JS and offer the objects 'pm' and 'postman',
required to interact with your requests/responses.

## Executing Tests
Once you wrote your tests simply execute a request or run all of a collection by choosing the 'Run'-option.
This will initiate a runner which goes through your tests linearly.

### Automating execution
To automate your tests (e.g. with every commit) I recommend the npm-package [newman](https://www.npmjs.com/package/newman). This allows for
the command 'newman run <-e your_env.json> <your_collection.json>', which can simply be used in your CLI.
<br>
There are numerous ways in which to use newman and I recommend just looking them up, depending on your needs.
Some are a docker-container or a cake add-in (C#). The run command also has a lot to offer, where I again
recommend you to just look at the documentation.