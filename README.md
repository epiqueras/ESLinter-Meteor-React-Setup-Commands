# ESLinter-Meteor-React-Setup-Commands
Setup commands for using ESLinter with Meteor and React.

## Run in root project directory:
1. ```meteor npm install --save-dev babel-eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-meteor eslint-plugin-react eslint-plugin-jsx-a11y eslint-import-resolver-meteor eslint```
2. ```eslint --init (optional)``` - Creates a configuration file.

## Add to package.json:
```
{
  ...
  "scripts": {
    "lint": "eslint .",
    "pretest": "npm run lint --silent"
  },
  "eslintConfig": {
    "parser": "babel-eslint",
    "parserOptions": {
      "allowImportExportEverywhere": true
    },
    "plugins": [
      "meteor"
    ],
    "extends": [
      "airbnb",
      "plugin:meteor/recommended"
    ],
    "settings": {
      "import/resolver": "meteor"
    },
    "rules": {}
  }
}
```
