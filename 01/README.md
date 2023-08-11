# 01

Install the required dependencies.

```console
npm install webpack webpack-cli -D
```

When running `npx webpack` it will create a `dist` directory.

It will work by default because we are using `./src/index.js` and it will generate a `./dist/main.js` file later.

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
