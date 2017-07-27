# Server Side Rendering

## Why

provide background information, problem description, challanges and/or goals

## What

The subject details, describe the tool / technology in detail, prefer linking to external sources if a 3rd party

## How

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

The **TELUS Digital context** of how we're using the described subject, provide **deep details** here, including usage manual, API documentation, operational guidelines, etc ...

## Who

`@` mention **teams** who are stakeholders or owners of described subject (see Github Members Groups)

## References

- [[link]] to internal references, and other wikis
- [[link]] to external references, documentation, product manuals and documentations
