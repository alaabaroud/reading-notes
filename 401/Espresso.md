# Read: 31 - Espresso

-it is the time to make tests for Android:
 **Espresso** is a testing framework for Android to make it easy to write reliable user interface tests. 
Espresso makes tests Such as expectations, interactions, and assertions and runs faster than the reqular tests. developers who love to make testing is the targetted people for espresso.

### Packages
- espresso-core:  Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.
- espresso-web: Contains resources for WebView support.
- espresso-idling-resource: Espresso's mechanism for synchronization with background jobs.
- espresso-contrib : External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.
- espresso-intents :Extension to validate and stub intents for hermetic testing.
- espresso-remote: Location of Espresso's multi-process functionality.

### How to make UI tests with Espresso:
 
 there are two main components that should be writter to make UI tests: UI interactions and assertions on View elements.
 to record UI test:
 - Click Run 
 - then Record Espresso Test.
 - choose the device on which you want to record the test.
 - click Ok.
 - --------------------------
 When you run the test, the Espresso test will try executing these actions in the same order.
 ![android](https://saucelabs.com/sauce-labs/images/espresso-test4.jpg)

