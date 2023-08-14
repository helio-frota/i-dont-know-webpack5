# Asset Management

> Text reduced based on official docs <https://webpack.js.org/guides/asset-management/#setup>

*Any time one file depends on another, webpack treats this as a dependency. This allows webpack to take non-code assets, such as images or web fonts, and also provide them as dependencies for your application.* ([source](https://webpack.js.org/concepts/dependency-graph/))

* Now we need `webpack.config.js` different from the very [basic example](../01/README.md)
* In order to import a CSS file, we need a thing called [loader](https://webpack.js.org/concepts/#loaders)
  * And we need to install more things `npm install style-loader css-loader -D`
* It scans the code looking for the css import. If we don't `import './foo.css';` inside of `index.js`, it does nothing.

## Install and run

```console
npm install ; npm run build
```
