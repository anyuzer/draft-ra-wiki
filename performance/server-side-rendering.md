# Server Side Rendering

## Why

Server Side Rendering is a key concept in the Telus Digital Reference Architecture, being one of the key reasons that React was initially adopted as a technology standard.

In many cases though, when a dependancy tree becomes deep enough, it may not be obvious to developers when they need to triage their application.

The purpose of this document is to provide some guidelines on when/how to triage Server Side Rendering.

## What

React Server Side Rendering is fast. Large complex applications, when optimized can be server side rendered quite easily under 50ms.

**IMPORTANT: IF YOUR APPLICATION IS RESPONDING SLOWLY IT IS PROBABLY NOT REACT**

To aid in this, in the isomorphic-starter-kit there is an automated warning that will get logged if your application is taking longer than 100ms to respond to.

This means the solution is not utilizing another tool or library, or attempting to add caching, or streaming to React to solve signficant slowness you may 

## How

The following code is some simple middleware you can use to see how long it takes for your Node process to receive a Request, and time to Response.

If you are using the Isomorphic Starter Kit, a warning comes prebuilt in and will automatically log if your SSR > 100ms
```js
// Simple Middleware for server.js to measure server side rendering time (ms)
app.use((req, res, next) => {
  let t = (new Date()).getTime();
  res.on('finish', ()=>{
    console.log(`${(new Date()).getTime() - t}ms ${req.url}`);
  });
  next();
});
```

To triage poor SSR do the following:
- Log the total time to response (ie. implement the above)
- Remove all of your API calls
- Compare the difference
- Look for any type of blocking loop you may be doing over a large or unknown dataset that could be slowing down your SSR
