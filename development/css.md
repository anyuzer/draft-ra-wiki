# CSS

## Why

Though every Telus web property uses CSS, developers rarely write CSS directly. CSS is often either included as part of [TDS components](http://tds.telus.com/), transpiled from [SCSS](./scss.md), or embedded in [JS](./javascript.md) components.

## What

Every front end site uses CSS in some shape or form at Telus. At the majority, CSS is the result of transpiled TDS components with SCSS source files. Now, components are utilising inline styles controlled by CSS-in-JS, or other variations of styled components.

## How

CSS can be written and maintained in many different ways. Developers at Telus are discouraged from writing CSS directly, and to instead go with the following options in order of preference:

1. Consume [React](./react.md) components from [TDS](http://tds.telus.com/)
2. Write [custom React components](./react.md#how)
3. Use SCSS

## References:
- [Mozilla Developer Network: CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [caniuse.com (Browser compatibility tables)](http://caniuse.com/) 
- [ITCSS](http://www.creativebloq.com/web-design/manage-large-css-projects-itcss-101517528)
- [Optimising the front end for the browser](https://dev.to/sanjsanj/optimising-the-front-end-for-thebrowser)
- [CSS Triggers](https://csstriggers.com/)
