# @handledom/in-template-string-loader

Compile Handledom templates in tagged template strings at build time.

## How to use

First, add `@handledom/in-template-string-loader` to a webpack config file:

```sh
npm install @handledom/in-template-string-loader --save-dev
```

In the `webpack.config.js` file, add this rule:

```js
  module.exports = {
    mode: 'development',
    entry: './src/index.js',
    output: {
      path: `${__dirname}/public`,
      filename: 'bundle.js'
    },
    module: {
      rules: [
        {
          test: /\.(js|ts)$/,
          exclude: /node_modules/,
          use: ['@handledom/in-template-string-loader']
        }
      ]
    }
  };
```

## Contribute

With VS Code, our recommanded plugin is:

* **TSLint** from Microsoft (`ms-vscode.vscode-typescript-tslint-plugin`)