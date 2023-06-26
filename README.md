# Test Automation Framework that supports Web and Mobile using WDIO, API using Supertest.
-------------------------------------------------------------------------------------------

## Tech Stack
- [WebdriverIO 7.##.#](https://webdriver.io/)
- [Supertest 6.#.#](https://www.npmjs.com/package/supertest)

## Language
- JavaScript

## Reporting
- Allure
- Junit
- Spec

## Test JS Framework
- Mocha


## Local Environment Setup (Mac OS)
- Install Node

  Run =>  `brew install node`

- Step 1: Install Appium

  Run =>  `brew install appium`

- Step 2: Install Appium Dependencies

  Run =>  `npm i -g appium`

- Step 3: Create Android Emulator

  Run =>   `$ANDROID_HOME/tools/bin/avdmanager create avd -n TestEmulator -d pixel --package "system-images;android-30;google_apis;x86"`

- Step 4: Create iOS Simulator

  Run => `xcrun simctl list`
  ( Note down the **UDID** of  **iOS v15.2  iPhone 12 mini**. This UDID will be later used in Package Json scripts to invoke Simulator )

### Local Environment Setup (Windows 10)
- Step 1: Install Node.JS

  `Download the .msi file and install it`

  `Click on Next and accept the license agreement`

  `Choose the nodejs folder on the next screen.`

  `Accept the defaults'`

  `Click next to begin the installation process.`

- Step 2: Create a Project Directory

- Step 3: Create Package.JSON
  
  `Install WebDriverIO command-line interface`

- Step 5: Create a WebDriverIO Config File

- Step 6: Create specs

- Step 7: Execute your tests

`Now, the WebdriverIO is ready for use!`

## Project Framework Setup in Local

- Clone the Repo from [GitHub](https://github.com/girlCoder8/single-ui-mobile-api-automation)

  Run => `git clone https://github.com/girlCoder8/single-ui-mobile-api-automation.git`

  Run => `npm install`


## Web and Mobile Test Cofigurations
- You can configure Web Automation ( i.e., Browser, Parallel Test, Retries, Device Farms, Reporting etc ) as per needs by editing [wdio.web.conf.js](https://github.com/Avinash-Kannan/webdriverio-supertest-framework/blob/main/test/config/wdio.web.conf.js) file.

- You can configure Mobile Automation ( i.e., Android/iOS, Parallel Test, Retries, Device Farms, Reporting etc ) as per needs by editing [wdio.android.conf.js](https://github.com/Avinash-Kannan/webdriverio-supertest-framework/blob/main/test/config/wdio.android.conf.js) and [wdio.ios.conf.js](https://github.com/Avinash-Kannan/webdriverio-supertest-framework/blob/main/test/config/wdio.ios.conf.js) files.


## Run Tests in Local
- Web  
  `npm run smoke-test-web`

- Mobile   
  `npm run regression-test-android`  
  `npm run smoke-test-ios`

- API  
  `npm run test-api`

## Test Tagging Mechanism
- using **mochaOpts.grep**  
  Prefix Smoke/Regression/Sanity/Custom tags to your Tests  
  Example : `it('regression smoke : should be able to order product from swag labs')`