# Chapter 7
This directory contains useful code snippets for the Automation Testing with Cypress Book chapter 7; 

In this chapter we will use an opensource application [(todomvc)](http://todomvc.com/examples/react/#/) to test the use of command line tools when running and debugging cypress tests.


## Executing Tests by folder
To execute tests in this chapter one needs to get into the chapter folder and run the tests from the test folder itself as every folder is a module on its own. 

```
$ cd chapter-7
```

### Installing project dependencies
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