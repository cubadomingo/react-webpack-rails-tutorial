Please see parent directory README.md.

Classes and React
=========================
We switched to ES6 Classes from React.createClass(). Thus your React components extend `React.Component`.

* [React.createClass Api](https://facebook.github.io/react/docs/top-level-api.html#react.createclass)
* [React ES6 Classes](https://facebook.github.io/react/docs/reusable-components.html#es6-classes)
* [How to Use Classes and Sleep at Night, Dan Abramov](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4)


ESLint
==========================
The `.eslintrc` file is based on the AirBnb [eslintrc](https://github.com/airbnb/javascript/blob/master/linters/.eslintrc).

It also includes many eslint defaults that the AirBnb eslint does not include.

Running linter:
===========================

Soon to be in gulpfile....but gulp-eslint depends on eslint depends on

```
    "eslint-plugin-react": "^2.0.2",
```

So don't use `npm run gulp lint` yet.

For now:

    bin/lint

Or (from either top level or within `client` directory)

    npm run lint


Updating Node Dependencies
===========================

```
yarn global add npm-check-updates
```

Then run this to update the dependencies (starting at the top level).

```
# Make sure you are in the top directory, then run:
cd client
rm yarn.lock
npm-check-updates -u
yarn install
```

Then confirm that the hot reload server and the rails server both work fine.

Adding Node Modules
=====================================
Suppose you want to add a dependency to "module_name"....

Before you do so, consider:

1. Do we really need the module and the extra JS code?
2. Is the module well maintained?

```bash
cd client
yarn add module_name@version
# or
# yarn add module_name@version --dev
```
