# Bulma with Reason for Dummies

## See Bulma [Docs](https://bulma.io/documentation/customize/with-webpack/)

Basically webpack points to `index.bs.js` and adds the `scss` to the dist folder.

You dont need this if you want to just use the simple stuff that you can get by adding the link tag to the head tag in `index.html`.

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.7.5/css/bulma.min.css" />
```

## Steps per Docs

1. create `src/mystyles.scss` and add minimum of

```css
@charset "utf-8";
@import "~bulma/bulma";
```

2. in `src/index.re` at top add

```reason
[%raw "require('./mystyles.scss')"];
```

3. see [webpack.config.js](./webpack.config.js) which calls `src/index.bs.js`.
