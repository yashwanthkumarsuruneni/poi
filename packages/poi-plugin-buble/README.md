# poi-plugin-buble

Use buble instead of babel to transpile `.js` `.es6` and script tag in `.vue` files

**ES2017 -> [buble](https://github.com/Rich-Harris/buble) -> [nodent](https://github.com/MatAtBread/nodent-compiler) for async/await -> ES5**

## Install

```bash
yarn add poi-plugin-buble --dev
```

## Usage

```js
// poi.config.js
module.exports = {
  plugins: [
    require('poi-plugin-buble')(/* options */)
  ]
}
```

Default Buble options:

```js
{
  transforms: {
    dangerousForOf: true,
    generator: false,
    modules: false
  },
  objectAssign: 'Object.assign'
}
```

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [pluginBuble](#pluginbuble)

### pluginBuble

Use Buble to transpile JS files

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
    -   `options.asyncAwait` **[Boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Enable async/await support via nodent (optional, default `true`)
    -   `options.bubleOptions` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** Options for buble.
        If this option is set, it will be assigned to default buble options.

## License

MIT © [EGOIST](https://github.com/egoist)