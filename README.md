# react-app-rewire-webpack-bundle-analyzer

> Add [`webpack-bundle-analyzer`](https://github.com/webpack-contrib/webpack-bundle-analyzer) to [`react-app-rewired`](https://github.com/timarney/react-app-rewired) config.

## Install

```sh
npm install --save-dev react-app-rewire-webpack-bundle-analyzer
```

## Usage

```js
const rewireWebpackBundleAnalyzer = require('react-app-rewire-webpack-bundle-analyzer')

module.exports = function override(config, env) {
  // ...

  if (env === 'production') {
    config = rewireWebpackBundleAnalyzer(config, env, {
      analyzerMode: 'static',
      reportFilename: 'report.html'
    })
  }

  return config
}
```

## License

MIT © [Bohdan Khodakivskyi](https://bohdan-khodakivskyi.com)
