# What's a BFF?
BFF stands for "Backend For Frontend". It's a term that's been discussed a lot as Microservices have grown in popularity. There are a number of articles out there describing the concept in more detail [1](http://samnewman.io/patterns/architectural/bff/) [2](https://www.thoughtworks.com/insights/blog/bff-soundcloud).

In the mobile app world, often the BFF is microservice that helps the app orchestrate and aggregate other domain services. 
 - The team that makes the app can control this service
 - They can put presentation logic in there that they want to change without re-publishing
 - If they are releasing both iOS and Android versions, some of the logic can go in the BFF helping out with [SRP](https://en.wikipedia.org/wiki/Single_responsibility_principle).

For web teams, it might be simpler just to think of this as "your application". Especially if you're building a standard web app - its going to orchestrate and aggregate access to various back end services to assemble view models, and could also provide endpoints for AJAX scripts or an SPA.

# What's the point of a BFF?
The main value we at TELUS digital hope to get from a BFF is release independence. Instead of waiting on another team to deploy a "hyrid" service that provides the aggregation we need, teams can simply build and deploy their own. 

# What should go in a BFF?
 Presentation logic, orchestration, and aggregation are usually the stock and trade of the BFF. Generally, if you're setting up an endpoint that other squads might need, consider getting it in to an API instead (see above).
 
# When should a BFF be shared amongst teams or squads?
The main point of the BFF is to unblock teams - instead of requesting that a services team creates a "hybrid" service that orchestrates or aggregates, the team can do this themselves.  When the BFF becomes shared, release independence is harmed, as you need to check with the other squad before you can ship. In general, to avoid this you wouldn't want to share a BFF between squads.

There might be an exception for situations where it does not increase release dependency, for instance squads that are really close to one another (shared product owner and close physical proximity) with syncrhonized or similar release goals and cadences.

# What if it would be useful for team A to make use of some code in team B's BFF?
Promote it to an API!
 - If there is an API that you could add the functionality to, find the owner and collaborate with them to move the functionality out.
 - Check the [API Inventory](https://docs.google.com/spreadsheets/d/1gXdfHANVBLTx_izdobsXBBwu5bw7ASKZpd1jy0jc3ok/edit#gid=0) to find what APIs are out there, or contact Royston or Ahmad.

# Testing notes
In the case of a traditional web app, or SPA where the SPA is deployed alongside the app or BFF, having good unit test coverage, along with some end to end testing asserting that things work together is likely to be fine in most cases. 

In mobile, or in other situations where its likely to have lots of different versions of the mobile app all in use and possibly talking to the same BFF at once, it would be valuable to generate functional tests that assert that the BFF still integrates with older but still supported versions of the app. This could be done with end to end testing of the older versions or a contract style test, which ever is easiest.

# Versioning notes
In the case that there are multiple clients (see notes above for one example) its useful to try to avoid breaking changes, follow semantic versioning, and other best practices.


# Notes around Isomorphic SPAs
Its becoming more and more common for teams to use a single node container for both the isomorphic version of an SPA and the BFF. Its important to continue to observe good isolation between tiers in this case, as usual. For instance, if the BFF has logic that allows connecting to a back end service, you wouldn't want the SPA trying to use that code, particularly from the browser - you'd want the SPA to talk to the BFF to get that data instead of bypassing it. In order to assert on this separation, some teams have used linting techniques.

# Does this represent a change in our thinking?
Previously, we'd been a bit overfocused on the BFF concept, particularly for SPAs. There had been talk of hosting your SPA on a CDN, and so on. This didn't particularly come to pass. The notion that the BFF is "just your app" is a new one meant to clean this up a bit and simplify things.