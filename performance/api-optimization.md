# API Optimization

## Why

A lot of the time, our applications will need to make API calls when we need data that is sourced by other systems within TELUS.  Every call has a page performance cost, yet we may want to incur the extra time to provide a richer experience to our customers.  We need to always have that in consideration when dealing with API calls.

## What

Currently we don't have any opinions and tools baked into our reference architecture.

- Log how long your API calls are taking to provide visibility in a consistent format (TBD)

## How

Some recommendations:  

- Try not to make calls that will block Server Side Render

- Maintain clear visibility on the number of calls that are made by the server and how long they take.

- If your API call is slow, escalate to your friendly API team! (APIs should not be slow)

- Cache reasonably static data on server with safe expiry! (ie. 5 minutes)

- Use internal network routing on the server side.


## Who

`@` mention **teams** who are stakeholders or owners of described subject (see Github Members Groups)

## References

- [[link]] to internal references, and other wikis
- [[link]] to external references, documentation, product manuals and documentations
