# Chapter 4
This directory contains useful code snippets for the Automation Testing with Cypress Book chapter 4; 

In this chapter we will use an opensource application [(todomvc)](http://todomvc.com/examples/react/#/) to test the use of command line tools when running and debugging cypress tests.

## Visiting Todo Application page

![visiting-application-page](https://user-images.githubusercontent.com/10160787/90381711-6dc3a800-e086-11ea-9739-9124e72d0fc7.gif)


## Asserting Element Exists on Todo Application

![asserting-todo-input-element](https://user-images.githubusercontent.com/10160787/90391973-b4b99980-e096-11ea-9d0c-24151785f7f6.gif)


## Adding an new Todo Item 

![adding a todo](https://user-images.githubusercontent.com/10160787/90876176-e8543680-e3aa-11ea-8a8f-a1615dc9be81.gif)


## Asserting added todo items exist

![asserting-state-change](https://user-images.githubusercontent.com/10160787/90876451-60226100-e3ab-11ea-87be-9eca4bcdd041.gif)


## Cypress disable file watching
This command, will disable the Cypress auto reload functionality when the files are changed. 

```
npm run cypress:run-disable-file-watching
```
# Installing Cypress on Windows
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