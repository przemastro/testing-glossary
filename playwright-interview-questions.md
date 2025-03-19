# Playwright Interview Questions

## Easy

### 1. **What is Playwright?**
**Answer:**  
Playwright is an open-source automation library for testing web applications. It provides capabilities to automate browsers (Chromium, Firefox, WebKit) for testing purposes, including interactions with the UI, API testing, and network conditions.

---

### 2. **Which browsers does Playwright support?**
**Answer:**  
Playwright supports Chromium, Firefox, and WebKit browsers, allowing you to test across multiple platforms and configurations.

---

### 3. **How do you install Playwright?**
**Answer:**  
You can install Playwright via npm with the following command:

    npm install playwright

### 4. **What are the core features of Playwright?**
**Answer:**  
Some of the core features of Playwright include:

Support for multiple browsers (Chromium, Firefox, WebKit)
Web automation for browser interaction
Page interactions (click, type, scroll, etc.)
API and network testing
Browser context management for multi-tab testing

### 5. **What is a Page object in Playwright?**
**Answer:**  
In Playwright, a Page represents a single tab in the browser. It allows you to perform actions like clicking, typing, and navigating on the page.

### 6. **How do you launch a browser in Playwright?**
**Answer:**  
You can launch a browser using the playwright.chromium.launch(), playwright.firefox.launch(), or playwright.webkit.launch() method:

javascript

    const { chromium } = require('playwright');
    const browser = await chromium.launch();

### 7. **What is the difference between .goto() and .click() methods in Playwright?**
**Answer:**  

    .goto(url) navigates to the given URL.
    .click(selector) clicks an element identified by the provided selector.

### 8. **How do you handle waits in Playwright?**
**Answer:**  
Playwright has built-in wait mechanisms that automatically wait for actions to complete, such as .waitForSelector(), .click(), .fill(), etc. It also supports manual waits using page.waitForTimeout(ms).

### 9. **How can you take a screenshot in Playwright?**
**Answer:**  
You can take a screenshot using the screenshot() method:

javascript

    await page.screenshot({ path: 'screenshot.png' });

### 10. **How do you run tests in parallel with Playwright?**
**Answer:**  
Playwright’s test runner supports parallel execution of tests with the help of the --workers option. The number of workers determines the number of tests running simultaneously.

bash

    npx playwright test --workers=4

## Moderate 

### 11. **How do you handle popups and alerts in Playwright?**
**Answer:**  
Playwright allows you to handle popups and alerts using event listeners. For example, for handling alerts:

javascript

    page.on('dialog', async dialog => {
      console.log(dialog.message());
      await dialog.accept();
    });

### 12. **What is a BrowserContext in Playwright?**
**Answer:**  
A BrowserContext represents an isolated browser session, which allows for multi-tab, multi-user testing in a single instance of a browser. Each context can have its own cookies, cache, and storage.

### 13. **How do you simulate mobile device testing in Playwright?**
**Answer:**  
Playwright allows you to simulate mobile devices using the emulate() method on the page:

javascript

    const iPhone = playwright.devices['iPhone 11'];
    const page = await context.newPage();
    await page.emulate(iPhone);

### 14. **How can you perform API testing with Playwright?**
**Answer:**  
Playwright supports network requests. You can intercept and make API calls using the page.route() method:

javascript

    page.on('route', route => {
      if (route.request().url().includes('api')) {
        route.continue();
      }
    });

### 15. **How do you handle cookies in Playwright?**
**Answer:**  
You can access and manipulate cookies using the context.cookies() and context.addCookies() methods:

javascript

    const cookies = await context.cookies();
    await context.addCookies([{ name: 'myCookie', value: '12345', domain: 'example.com' }]);

### 16. **What is the use of page.locator() in Playwright?**
**Answer:**  
page.locator() is used to locate elements on the page. It allows for more stable, reusable selectors and supports waiting for the element to be visible before performing actions.

javascript

    const button = page.locator('#submit');
    await button.click();

### 17. **How do you handle file uploads in Playwright?**
**Answer:**  
You can handle file uploads by using the setInputFiles() method:

javascript

    const fileInput = page.locator('input[type="file"]');
    await fileInput.setInputFiles('path/to/file.png');

### 18. **How do you run a specific test file in Playwright?**
**Answer:**  
You can run a specific test file by passing the path to the test file:

bash

    npx playwright test tests/example.spec.js

### 19. **What is Playwright Test Runner and how do you use it?**
**Answer:**  
Playwright Test Runner is an integrated test runner that comes with Playwright. It provides features like parallel testing, test retries, and automatic waiting. You can use it to write and execute tests.

bash

    npx playwright test

### 20. **How do you capture network traffic in Playwright?**
**Answer:**  
You can capture network traffic by listening to the page.on('route') event to intercept requests and responses:

javascript

    page.on('route', route => {
      console.log(route.request().url());
    });


## Difficult

### 21. **How do you handle authentication in Playwright?**
**Answer:**  
You can handle authentication by setting cookies or using the page.setRequestInterceptor() method to inject authentication tokens into requests.

javascript

    await page.setCookie({ name: 'authToken', value: 'yourAuthToken', domain: 'example.com' });

### 22. **How do you wait for a specific element to appear in Playwright?**
**Answer:**  
You can use locator.waitFor() or page.waitForSelector() to wait for an element to appear on the page:

javascript

    await page.waitForSelector('button#submit', { state: 'visible' });

### 23. **How do you handle situations where an element is dynamically generated in Playwright?**
**Answer:**  
You can use locator.waitFor() or explicitly wait for elements with await page.waitForSelector() to ensure the element is available before interacting with it.

### 24. **How do you perform cross-browser testing with Playwright?**
**Answer:**  
You can perform cross-browser testing by configuring Playwright to run on different browsers (Chromium, Firefox, WebKit). You simply need to specify the desired browser when launching the test:

javascript

    const { firefox, webkit } = require('playwright');
    const browser = await firefox.launch();

### 25. **How do you set up Playwright for CI/CD pipelines?**
**Answer:**  
You can set up Playwright for CI/CD by installing Playwright and its dependencies on your CI server, configuring your test scripts, and running them in the pipeline. Additionally, you can set up Playwright in Docker to ensure a consistent testing environment.

### 26. **How do you run tests on multiple devices with Playwright?**
**Answer:**  
Playwright allows running tests on multiple devices by creating multiple contexts and launching the tests simultaneously:

javascript

    const { devices } = require('playwright');
    const iphone = devices['iPhone 11'];
    const context1 = await browser.newContext({ ...iphone });
    const context2 = await browser.newContext();

### 27. **How do you debug tests in Playwright?**
**Answer:**  
You can debug Playwright tests by using the --debug flag or pausing the test execution with await page.pause() to inspect the state of the browser. You can also use console.log() or the Playwright Inspector for better insights.

### 28. **How do you implement retries for failed tests in Playwright?**
**Answer:**  
You can implement retries for failed tests by using the retries option in the test configuration:

javascript

    module.exports = {
      retries: 2
    };

### 29. **How do you handle browser crashes or exceptions in Playwright?**
**Answer:**  
You can handle browser crashes or exceptions by using try-catch blocks in your tests or by listening to the browser.on('disconnected') event to handle unexpected crashes and reconnect or restart the browser.

### 30. **How do you manage test data for Playwright tests?**
**Answer:**  
Test data management in Playwright can be achieved by using mock data, creating separate test environments, or setting up initial conditions before each test using beforeEach() hooks. You can also seed databases or interact with APIs to set up test data before running the tests.
