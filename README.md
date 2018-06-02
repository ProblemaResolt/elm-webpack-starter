<img src="https://circleci.com/gh/simonh1000/elm-webpack-starter.png?circle-token=:circle-token">

# Elm 0.18 with Webpack 4, Hot Reloading & Babel 7

Elm dev environment with hot-loading (i.e. state is retained as you edit your code - Hot Module Reloading, HMR)). I use this daily for my professional work. Like elm-community/elm-webpack-starter but using Webpack 4.

## Installation

Clone this repo into a new project folder and run install script.
(I ignore the errors about missing jquery as it is best not to use the Bootstrap jquery-based components with Elm)
(You will probably want to delete the .git/ directory and start version control afresh.)

With npm

```sh
$ git clone git@github.com:simonh1000/elm-webpack-starter.git new-project
$ cd new-project
$ npm install
$ npm run dev
```

With yarn
```sh
$ git clone git@github.com:simonh1000/elm-webpack-starter.git new-project
$ cd new-project
$ yarn
$ yarn dev
 ```

Open http://localhost:3000 and start modifying the code in /src.
(An example using Routing is provided in the `navigation` branch)

## Production

Build production assets (js and css together) with:

```sh
npm run prod
```

## Static assets

Just add to `src/assets/` and the production build copies them to `/dist`

## Testing

[Install elm-test globally](https://github.com/elm-community/elm-test#running-tests-locally)

`elm-test init` is run when you install your dependencies. After that all you need to do to run the tests is

```
yarn test
```

Take a look at the examples in `tests/`

If you add dependencies to your main app, then run `elm-test --add-dependencies`

I have also added [elm-verify-examples](https://github.com/stoeffel/elm-verify-examples) and provided an example in the definition of `add1` in App.elm.

<hr />

## ES6

This starter includes [Babel](https://babeljs.io/) so you can directly use ES6 code.

## Changelog

 - 1.2.0 - Webpack 4, Babel 7
 - 1.1.0 - add elm-verify-examples

 ## Credits

 A long time ago this code was forked from https://github.com/fluxxu/elm-hot-loader


 ## How it works

 `webpack-dev-server --hot --inline --host=0.0.0.0 --port 3000`

  - hot Enable webpack's Hot Module Replacement feature
  - inline (default) a script will be inserted in your bundle to take care of reloading, and build messages will appear in the browser console.
  - host=0.0.0.0 - enable you to reach your dev environment from another device - e.g  your phone
  - port 3000 - use port 3000 instead of default 8000
