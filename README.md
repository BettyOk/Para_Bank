ParaBank Website Testing with Cypress and Cucumber BDD

Project Title and Description

    ParaBank Website Test** is a project that automates the testing of the ParaBank website ([ParaBank](https://parabank.parasoft.com/parabank/index.htm)) using **Cypress** and **Cucumber** for behavior-driven development (BDD). This setup allows for writing and executing tests in **Gherkin** syntax, providing a robust framework for end-to-end testing of web applications.

Prerequisites

    Before setting up the project, the following tools should be installed:

    - Node.js: [Download and install Node.js](https://nodejs.org/)
    - Cypress: Install Cypress via npm
    - Cucumber Preprocessor: Install necessary packages for Cucumber support

Installation

    1. Clone the Project

    Clone the repository or create a new project folder.

    ```bash
    git clone https://github.com/BettyOk/Para_Bank.git
    cd Para_Bank
    ```

    2. Install Dependencies

    Run the following command to install the project dependencies:

    ```bash
    npm install
    ```

    The following dependencies are included in the `package.json`:

    - `cypress`
    - `@badeball/cypress-cucumber-preprocessor`
    - `@bahmutov/cypress-esbuild-preprocessor`
    - `@shelex/cypress-allure-plugin`

    3. Cypress Configuration

    The `cypress.config.js` is correctly configured for **Cucumber** and other plugins.

Project Structure

    Feature Files

    Located in `cypress-bdd-template-main/cypress/e2e/features/`:
    - `login.feature`
    - `register.feature`

    Step Definitions

    Located in `cypress-bdd-template-main/cypress/e2e/steps_definitions/`:
    - `loginTests.spec.js`
    - `registerTests.spec.js`

    Page Object Files

    Located in `cypress-bdd-template-main/cypress/pages/`: 
    - `loginPage.js`
    - `registerPage.js`

    Running the Tests

    1. Execute Tests

    Run Cypress tests using the following command:

    ```bash
    npx cypress run
    ```

    This will execute all feature files specified in the `specPattern` of the `cypress.config.js` and generate reports in the configured format.

    2. View Test Reports

    - Mocha HTML Report: Located in the `results` directory, usually named `mochawesome.html`.  
      Open the HTML report in a web browser to review the detailed test results.

    Environment Configuration

    The necessary environment variables are set for the tests, such as `USERNAME`, `PASSWORD`, and `VALIDUSERNAME`.  
    Location: `cypress-bdd-template-main/cypress.env.json`

Continuous Integration

    This project is integrated with GitHub Actions for continuous integration. The GitHub repository is available at [https://github.com/BettyOk/Para_Bank].  
    CI configuration is located in the `.github/workflows` directory.
