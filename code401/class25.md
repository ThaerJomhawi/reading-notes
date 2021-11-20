# Espresso

Espresso is an Android UI tests. Espresso tests state expectations, interactions, and assertions clearly without the distraction of boilerplate content, custom infrastructure, or messy implementation details getting in the way.

### Synchronization capabilities

Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

- The message queue is empty.
- There are no instances of AsyncTask currently executing a task.
- All developer-defined idling resources are idle.

## Create UI tests with Espresso Test Recorder

The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.

> **Before using Espresso Test Recorder, make sure you turn off animations on your test device to prevent unexpected results.**

### Record an Espresso test

1. Click Run > Record Espresso Test.

2. In the Select Deployment Target window, choose the device on which you want to record the test.

3. Recorded interactions will appear in the main panel in the Record Your Test window, When you run the test, the Espresso test will try executing these actions in the same order.

### Add assertions to verify UI elements

1. Click Add Assertion.
2. To select a View element on which to create an assertion, click on the element in the screenshot or use the first drop-down menu in the Edit assertion box at the bottom of the window.
3. Select the assertion you want to use from the second drop-down menu in the Edit assertion box.
4. Click Save and Add Another to create another assertion or click Save Assertion to close the assertion panels.

### Save a recording

1. Click Complete Recording.
2. Use the Test class name text field if you want to change the suggested name. Click Save.
3. Android Studio shows the test class as selected in the Project window of the IDE.