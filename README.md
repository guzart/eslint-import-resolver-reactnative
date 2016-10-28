# eslint-import-resolver-reactnative

[![npm](https://img.shields.io/npm/v/eslint-import-resolver-reactnative.svg)](https://www.npmjs.com/package/eslint-import-resolver-reactnative)

React Native module resolution plugin for [`eslint-plugin-import`](https://www.npmjs.com/package/eslint-plugin-import).

Uses [`eslint-import-resolver-node`](https://www.npmjs.com/package/eslint-import-resolver-node) with a few modifications:

  * Configures extensions for React Native `['.js', '.json', '.android.js', '.ios.js']`
  * Helps resolve project name paths to the root ([`eslint-plugin-import#626`](https://github.com/benmosher/eslint-plugin-import/issues/626))

