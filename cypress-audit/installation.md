## Installation

🍔 In order to make the `cy.lighthouse()` command available in your project, there are **3 steps to follow:**

### Installing the dependency
In your favorite terminal:
```
yarn add -D @cypress-audit/lighthouse
# or
npm install --save-dev @cypress-audit/lighthouse
```

### The Server Configuration
By default, if you try to run Lighthouse from the command line (or from Nodejs), you will see that it opens a new web browser window by default. As you may also know, Cypress also opens a dedicated browser to run its tests.

The following configuration allows Lighthouse and Cypress to make their verifications inside **the same browser (controlled by Cypress) instead of creating a new one.**

### Cypress over v10
In the `cypress.config.js` file, make sure to have:
```
const { lighthouse, prepareAudit } = require("@cypress-audit/lighthouse");
const { pa11y } = require("@cypress-audit/pa11y");

module.exports = {
  e2e: {
    baseUrl: "http://localhost:3000", // this is your app
    setupNodeEvents(on, config) {
      on("before:browser:launch", (browser = {}, launchOptions) => {
        prepareAudit(launchOptions);
      });

      on("task", {
        lighthouse: lighthouse(),
        pa11y: pa11y(console.log.bind(console)),
      });
    },
  },
};
```

### Cypress prior to v10
In the `cypress/plugins/index.js` file, make sure to have:
```
const { lighthouse, prepareAudit } = require("@cypress-audit/lighthouse");

module.exports = (on, config) => {
  on("before:browser:launch", (browser = {}, launchOptions) => {
    prepareAudit(launchOptions);
  });

  on("task", {
    lighthouse: lighthouse(), // calling the function is important
  });
};
```

### Making Cypress aware of the commands
When adding the following line in the `cypress/support/command.js` file, you will be bale to use `cy.lighthouse` inside your Cypress tests:
```
import "@cypress-audit/lightouse/commands";
```
You can then call `cy.lighthouse()` in your Cypress tests.

![image](https://user-images.githubusercontent.com/85356433/227227511-c5559c81-3c1a-450f-9c05-1b73f7d9102e.png)

