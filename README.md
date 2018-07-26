# eslint-import-resolver-reactnative

[![npm](https://img.shields.io/npm/v/eslint-import-resolver-reactnative.svg)](https://www.npmjs.com/package/eslint-import-resolver-reactnative)

React Native module resolution plugin for [`eslint-plugin-import`](https://www.npmjs.com/package/eslint-plugin-import).

Uses [`eslint-import-resolver-node`](https://www.npmjs.com/package/eslint-import-resolver-node) with a few modifications:

  * Configures extensions for React Native `['.js', '.json', '.android.js', '.ios.js', '.ts', '.tsx']`
  * Helps resolve project name paths to the root ([`eslint-plugin-import#626`](https://github.com/benmosher/eslint-plugin-import/issues/626))


## Usage

```bash
npm install --save-dev eslint-import-resolver-reactnative
```

Configure ESLint to use this plugin.

```
// .eslintrc
settings:
  import/resolver: reactnative
```

Use your project's name as part of the import path.

```
// package.json
{
  "name": "cool-project"
}
```

```
import Button from 'cool-project/components/button';
// imports a file located at <PROJECT_ROOT>/components/button.js (or button.android.js or button.ios.js)

// ...
```

Notice that this plugin will resolve your project's name to your project's root folder.
