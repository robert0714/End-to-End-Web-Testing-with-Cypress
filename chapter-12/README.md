# Chapter 12
This directory contains useful code snippets for the Automation Testing with Cypress Book chapter 12;

We have bootstrapped our tests with the [Cypress realworld application](https://github.com/cypress-io/cypress-realworld-app) project which is a simple financial application
that is meant to help Cypress users better understand how to test Cypress applications. The application is located in the root location in the directory `cypress-realworld-app`. 

To simplify execution of the application, we will only have three commands that will be used to run our test application. One command is to run to install the dependencies, the other to run the application, while the last command's purpose will be to reset the application as it uses a json database which needs resetting if at all any 
changes were made to the database in the process.

## Application Summary
The Application is a React Typescript application with the backend built with express Js and the database low-db.

## 1. Installing  Yarn 
This command will install yarn package manager in your machine globally
N.B This might require you to run with Sudo permissions e.g. `sudo npm install -g yarn`

```
npm install -g yarn

```

## 2. Installing our application dependencies

This command will install our test application dependencies and start our application (both the API and the frontend)

```
npm run cypress-init (Linux and MacOS)

```

```
npm run cypress-init-windows (Windows OS)

```
### Prerequisites

The only requirement for this project is to have [Node.js](https://nodejs.org/en/) **version 18** installed on your machine. Refer to the [.node-version](./.node-version) file for the exact version.

The only requirement for our application is to have [Node.js](https://nodejs.org/en/) **version 12** installed on your machine. Refer to the [.node-version](../cypress-realworld-app/.node-version) file for the exact version.

#### switch npm

```bash
( using for cypress-realworld-app)
nvm install 12.22.12
nvm list
nvm current 
nvm use  12.22.12

( using for chapter 10)
nvm install 18.17.1
nvm list
nvm current 
nvm use  18.17.1
```
## 3. Running the application

This command will run our test application and start both the frontend and backend (API) and seed our low-db data. 

```
npm run cypress-app (Linux and Mac OS)

```

```
npm run cypress-app-windows ( Windows OS)

```

## 4. Resetting the application

This command will reset our low-db database to the original state without any additions that may have been made during the process of interaction with our application. 

```
npm run cypress-app-reset (Linux and Mac OS)

```

```
npm run cypress-app-reset (Windows OS)

```

### Application test usernames

Katharina_Bernie 
Tavares_Barrows
Allie2
Giovanna74

All usernames have a password of `s3cret`



## Executing Tests by folder
To execute tests in this chapter one needs to get into the chapter folder and run the tests from the test folder itself as every folder is a module on its own. 

```
$ cd chapter-12
```

### Installing project dependencies for Cypress tests
```
$ npm install

or 

$ npm ci

```

### Running all Cypress Tests
```
$ npm run cypress:run
```

### Adding Percy Token (Unix)
```
export PERCY_TOKEN=YOUR_TOKEN_HERE
```

### Adding Percy Token (Windows)
```
set PERCY_TOKEN=YOUR_TOKEN_HERE
```
### Adding Applitools Token (Unix)
```
export APPLITOOLS_API_KEY=YOUR_API_KEY_HERE
```

### Adding Applitools Token (Windows)
```
set APPLITOOLS_API_KEY=YOUR_API_KEY_HERE
```


# Visual Testing
## Official Documentation
* https://docs.cypress.io/guides/tooling/visual-testing
* https://docs.cypress.io/plugins#visual-testing
* Cypress plugins ?
  * Cypress Configureation(Legacy) : https://docs.cypress.io/guides/references/legacy-configuration#Plugins
  * [The **setupNodeEvents**  function](https://docs.cypress.io/guides/references/configuration#setupNodeEvents) was added in Cypress version ``10.0.0`` to replace the deprecated [plugins file](https://docs.cypress.io/guides/references/legacy-configuration#Plugins).


### Percy (@percy/cypress)
* reference: https://docs.percy.io/docs/cypress
* sample code: https://github.com/percy/example-percy-cypress

#### Setting up Percy
* Setting up Percy is not complicated and involves the following steps:

1. Create an account with BrowserStack (https://www.browserstack.com/).
2. Verify your BrowserStack email address.
3.  Create an organization in the Browserstack dashboard.
4. Log into the Percy dashboard using your BrowserStack account.
5. Create a project on the Percy dashboard.
6. Configure Percy on your local project using the instructions on the Percy website (https://docs.percy.io/docs/cypress).
7. Add a **Percy TOKEN** to your local machine as an environment variable.
8. Voila! You are now ready to write your tests!

Once steps 1 - 4 have been completed, Percy provides you with a **TOKEN** that ⚠ **you must add to your machine environment variable before executing your tests**. You can visit the Percy documentation (https://docs.percy.io/docs/cypress) for more information on how to set up Percy using Cypress.


####  Step by Step guide to migrating visual regression test project to the latest Percy SDK+
##### Step 1: Launch the Percy migration tool

The **@percy/migrate** tool is useful in migrating your visual validation project to the latest Percy CLI. Use the below command to launch the migration tool.

```bash
npx @percy/migrate
```

##### Step 2: Choose the best possible option in CLI

When you launch the CLI migration tool, it automatically detects the Percy SDK, which you are using, such as **@percy/cypress**, @percy/puppeteer, @percy/webdriverio, etc. Typically below set of questions will be asked.

Are you currently using **@percy/cypress** ? Answer **Yes**




### Applitools (@applitools/eyes-cypress)
* reference: https://applitools.com/tutorials/quickstart/web/cypress
* sample code: https://github.com/applitools/example-cypress-javascript
#### Setting up Applitools
* Just like Percy, the Applitools Eyes SDK is relatively easy to set up with Cypress. This can be achieved by performing the following steps:

1. Create an account with Applitools (https://auth.applitools.com/users/register).
2. Verify your Applitools email address.
3. Navigate to the Applitools dashboard to obtain the API key.
4. Configure Applitools on your local project.
5. Add the Applitools **APPLITOOLS_API_KEY** to your local machine as an environment variable.
6. Party!
Once steps 1 and 2 have been completed, Applitools provides you with an **APPLITOOLS_API_KEY**, similar to the Percy TOKEN, that  ⚠ **you must add as an environment variable to your machine before executing your tests**. You can visit the Applitools and Cypress documentation (https://applitools.com/tutorials/cypress.html) to find out more about how to set up the Applitools Eyes SDK using Cypress.
