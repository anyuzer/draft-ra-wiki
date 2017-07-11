# CSS

## Why

CSS is an interesting language for having the perception of being easy to learn, yet difficult to scale and modularize. Front end teams often re-use the same CSS and want to be able to revisit a codebase months later to easily make changes.

## What

CSS is Cascading Style Sheets. At a glance:

- Objects in the DOM are selected and styled using CSS selectors with corresponding properties and values.

Example:
```css
.card {
  max-width: 200px;
  border: 1px solid #000;
  background-color: #fff;
}
```

Recommended resources:
- CSS reference: [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- Browser compatibility tables: [caniuse.com](http://caniuse.com/)

## How

First and foremost, using a preprocessor such as SCSS (see [guideline for SCSS](./scss.md)) is strongly encouraged since it offers many benefits such as variables, mixins, nested selectors, and modular file importing.

:construction: _Work in progress_

### Structural Paradigms

Though there are many useful structural paradigms such as BEM to organise your CSS selectors, we recommend [ITCSS](http://www.creativebloq.com/web-design/manage-large-css-projects-itcss-101517528)

### Optimisations

Keep the following in mind when developing CSS:

- The browser builds the CSSOM as CSS files are parsed (see [Optimising the front end for the browser](https://dev.to/sanjsanj/optimising-the-front-end-for-thebrowser)), and it is important to minimise those steps to avoid rebuilding the CSSOM. One way to get around that is to **minify and concatenate your CSS**.
- Animations and transitions are useful, but they are not always performant. Avoid transitioning paint-heavy properties. Here is a convenient list: [CSS Triggers](https://csstriggers.com/).
