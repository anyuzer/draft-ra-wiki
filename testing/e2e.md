# End to End testing

## Why

When our application gets deployed through our [Continuous Delivery](../delivery/continuous-delivery.md) pipeline, we want to know that an application is working when it is deployed to our pre-production and production environments.

## What

Even though unit tests are passing, there may be issues with the application startup, or the deployment configuration, or in the downstream dependencies, which keeps our application from working. An End to End test is a type of test that runs an automated functional test over the entire scope of our application, which simulates how our clients will be using our application, to ensure that the features remain working, even when integrating with live downstream services and external interfaces.

## How

Our [starter kits](../development/starter-kits.md) ship out of the box with an End to End testing step as part of their delivery pipeline.

### API

API's shall be end-to-end tested using node-fetch, to query the API endpoints and verify that they are working. Authenticated APIs should be able to log in, in order to test secured endpoints.

### UI

UI's shall be end-to-end tested using [Nightwatch.js](http://nightwatchjs.org/). Nightwatch runs an automated Chrome web browser against our deployed user interface, and tests the application as a user would, by browsing through the pages, clicking links, and filling out forms.

#### Saucelabs

TODO

#### Device lab

TODO

## Who

@delivery @qa

## References

- [Nightwatch.js](http://nightwatchjs.org/)