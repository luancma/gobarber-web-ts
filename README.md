## REACT ESLINT/PRETTIER CONFIG

### ISNTALL LIBS:

##### Eslint/Prettier

```
yarn add eslint prettier eslint-config-prettier eslint-plugin-prettier eslint-import-resolver-typescript -D
```

##### Prettier config:

prettier.config.js

```javascript
module.exports = {
  singleQuote: true,
  trallingComma: 'all',
  allowParens: 'avoid',
};
```

##### Eslint config:

.eslintrc.json

```json
{
  "env": {
    "browser": true,
    "es6": true
  },
  "extends": [
    "plugin:react/recommended",
    "airbnb",
    // new
    "plugin:@typescript-eslint/recommended"
  ],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  },
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": 11,
    "sourceType": "module"
  },
  "plugins": [
    "react",
    "@typescript-eslint",
    // new
    "@typescript-eslint"
  ],
  "rules": {
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exaustive": "warn",
    "react/jsx-filename-extension": [1, { "extensions": [".tsx"] }],
    "import/prefer-default-export": "off",
    "import/extensions": [
      "error",
      "ignorePackages",
      {
        "ts": "never",
        "tsx": "never"
      }
    ]
  },
  "settings": {
    "import/resolver": {
      "typescript": {}
    }
  }
}
```
