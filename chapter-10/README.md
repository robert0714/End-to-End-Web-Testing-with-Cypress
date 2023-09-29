# Chapter 10
This directory contains useful code snippets for the Automation Testing with Cypress Book chapter 10;

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
$ cd chapter-10
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




# Installing Cypress 
* Referecne: https://docs.cypress.io/guides/getting-started/installing-cypress
## Using Yarn
* With the following command:
  ```bash
  $ yarn add cypress -dev
  ``` 
## Using NPM
* With the following command:
  ```bash
  $ npm install cypress --save-dev
  ``` 
# Opening Cypress
* Referecne: https://docs.cypress.io/guides/getting-started/opening-the-app
## Runing with Yarn
* Run the following command:
  ```bash
  $ yarn run cypress open
  ``` 
## Runing with Npx
* Run the following command:
  ```bash
  $ npx cypress open
  ``` 
## Runing with the node modules path
### Launching Cypress using the full path
* The installed Cypress executable is located in **node_modules**. We can use the following command:
  ```bash
  $ ./node_modules/.bin/cypress open
  ``` 
### Launching Cypress using the shortcut
  ```bash
  $ (npm bin)/cypress open
  ```
# Switching browsers
* Referecne: https://docs.cypress.io/guides/guides/cross-browser-testing
* All Chromium-based browsers, Edge, and Firefox can be launched using the command line wiyh the following command:
  ```bash
  $ cypress run --browser {browser-name}
  ```
# Migration Cypress scirpt
## Cypress Update
  ```bash
  $ npm i npm-check-updates
  $ node_modules\.bin\ncu
  $ node_modules\.bin\ncu -u
  ```
## Migration Cypress script
  ```bash
  There is a cypress.json file at the path: ....
  To address all issues, run:
  Cypress version 10.0.0 no longer supports cypress.json.
  Please run cypress open to launch the migration tool to migrate to cypress.config.{js,ts,mjs,cjs}. 
  ```
* Yes ! excute**cypress open**
# Print DEBUG logs
* Reference: https://docs.cypress.io/guides/references/troubleshooting#Print-DEBUG-logs
* Cypress is built using the debug module. That means you can receive helpful debugging output by running Cypress with this turned on. **Note**: you will see a LOT of messages when running with ``DEBUG=...`` setting.
  * On Mac or Linux:
    ```bash
    DEBUG=cypress:* cypress run
    ```
  * On Windows:
    On Windows, you'll need to run the command in a command prompt terminal (not PowerShell).
    ```bash
    set DEBUG=cypress:*
    cypress run
    ```
* If you have issues with the logs not printing, it may be a permissions issue with setting the environment variable in your terminal. You may need to run your terminal in administrative mode or review your permission settings.

* Read [more about the CLI](https://docs.cypress.io/guides/guides/command-line#Debugging-commands) options here and [Good Logging](https://glebbahmutov.com/blog/good-logging/) blog post.