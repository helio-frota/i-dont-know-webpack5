# Development

This is related to the development mode.

*When webpack bundles your source code, it can become difficult to track down errors and warnings to their original location. For example, if you bundle three source files (a.js, b.js, and c.js) into one bundle (bundle.js) and one of the source files contains an error, the stack trace will point to bundle.js. This isn't always helpful as you probably want to know exactly which source file the error came from.*

*In order to make it easier to track down errors and warnings, JavaScript offers source maps, which map your compiled code back to your original source code. If an error originates from b.js, the source map will tell you exactly that.* ([source](https://webpack.js.org/guides/development/#using-source-maps))

We can enable those things in the `webpack.config.js` file:

```js
mode: 'development',
devtool: 'inline-source-map',
```

We can use some approaches in development mode like:

* A) webpack's Watch Mode
* B) webpack-dev-server
* C) webpack-dev-middleware

For **A** we just this this `"watch": "webpack --watch",` in `package.json` scripts section.

For **B** we need:

Install `npm install webpack-dev-server -D`

Add this to `webpack.config.js`:

```js
devServer: {
  static: './dist',
},
optimization: {
  runtimeChunk: 'single',
},
```

That chunk part is related to [code splitting](https://webpack.js.org/guides/code-splitting/).

Also we need to add this to scripts section in `package.json` file `"start": "webpack serve --open",`
