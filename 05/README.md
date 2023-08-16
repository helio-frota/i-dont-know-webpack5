# TypeScript

```console
npm install ts-loader -D
```

Configure `webpack.config.js` adding the `ts-loader` rule and the `resolve` section:

```js
module: {
  rules: [ 
    {
      test: /\.tsx?$/,
      use: 'ts-loader',
      exclude: /node_modules/,
    },
  ],
},
resolve: {
  extensions: ['.tsx', '.ts', '.js'],
},
```
