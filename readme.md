mCurrentFocus=Window{bd38736 u0 com.google.android.deskclock/com.android.deskclock.DeskClock}

npm install --save-dev @wdio/allure-reporter allure-commandline


reporters: [
    ['allure', {
        outputDir: 'allure-results',
        disableWebdriverStepsReporting: true,
        disableWebdriverScreenshotsReporting: false,
        useCucumberStepReporter: true
    }]
    ],


allure serve allure-results


afterScenario: async function (world, result) {
    if (result.passed === false) {
        await browser.takeScreenshot();
    }
    },

await browser.takeScreenshot();


npm install rimraf --save-dev


npx wdio run wdio.conf.js

npx wdio run wdio.conf.js --cucumberOpts.tagExpression="@addAlarm"

npm run clean:allure && npx wdio run wdio.conf.js --cucumberOpts.tagExpression="@ addAlarm "
