# Getting Started

> Text reduced based on official docs <https://webpack.js.org/guides/getting-started/#basic-setup>

* We can interact with webpack via CLI or API. But for this repository we are going to use the CLI and mostly using the webpack configuration file.
* This is using the defaults, and since this is a really basic example it will create the `dist` directory with a file inside of it called `main.js`, nothing more than that, all the rest is just boring theory. The `npx webpack` command will take the script at `src/index.js` as the `entry point`, and will generate `dist/main.js` as the `output`.

Because of these defaults, we **don't** need a `webpack.config.js` file with the following content:

```js
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
}
```

## Install and run

```console
npm install ; npx webpack
```

In case we create a different filename other than `./src/index.js` we are going to get an error like this:

```console
ERROR in main
Module not found: Error: Can't resolve './src' in '/code/hands-on-webpack5/01'
resolve './src' in '/code/hands-on-webpack5/01'
  using description file: /code/hands-on-webpack5/01/package.json (relative path: .)
    Field 'browser' doesn't contain a valid alias configuration
    using description file: /code/hands-on-webpack5/01/package.json (relative path: ./src)
      no extension
        Field 'browser' doesn't contain a valid alias configuration
        /code/hands-on-webpack5/01/src is not a file
      .js
        Field 'browser' doesn't contain a valid alias configuration
        /code/hands-on-webpack5/01/src.js doesn't exist
      .json
        Field 'browser' doesn't contain a valid alias configuration
        /code/hands-on-webpack5/01/src.json doesn't exist
      .wasm
        Field 'browser' doesn't contain a valid alias configuration
        /code/hands-on-webpack5/01/src.wasm doesn't exist
      as directory
        existing directory /code/hands-on-webpack5/01/src
          using description file: /code/hands-on-webpack5/01/package.json (relative path: ./src)
            using path: /code/hands-on-webpack5/01/src/index
              using description file: /code/hands-on-webpack5/01/package.json (relative path: ./src/index)
                no extension
                  Field 'browser' doesn't contain a valid alias configuration
                  /code/hands-on-webpack5/01/src/index doesn't exist
                .js
                  Field 'browser' doesn't contain a valid alias configuration
                  /code/hands-on-webpack5/01/src/index.js doesn't exist
                .json
                  Field 'browser' doesn't contain a valid alias configuration
                  /code/hands-on-webpack5/01/src/index.json doesn't exist
                .wasm
                  Field 'browser' doesn't contain a valid alias configuration
                  /code/hands-on-webpack5/01/src/index.wasm doesn't exist
```
