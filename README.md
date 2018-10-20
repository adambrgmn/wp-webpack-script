<p align="center">
  <a href="https://wpack.io"><img width="600" height="130" src="https://raw.githubusercontent.com/swashata/wp-webpack-script/master/assets/wpackio-logo.png"></a>
</p>

# wpack.io - Modern JavaScript tooling for WordPress

[![Build Status](https://travis-ci.com/swashata/wp-webpack-script.svg?branch=master)](https://travis-ci.com/swashata/wp-webpack-script) [![codecov](https://codecov.io/gh/swashata/wp-webpack-script/branch/master/graph/badge.svg)](https://codecov.io/gh/swashata/wp-webpack-script) [![npm version](https://badge.fury.io/js/%40wpackio%2Fscripts.svg)](https://badge.fury.io/js/%40wpackio%2Fscripts)

## What is wpack.io?

Put simply, wpack.io is a nodejs based build tool to ease up using modern javascript
in WordPress Themes and Plugins. It gives a fine _Developer Experience_ (DX) and
a single dependency for all your bundling requirement.

> It is a fine-tuned webpack/browser-sync configuration made specifically for
> WordPress Theme and Plugin Development.

With the rise of Gutenberg editor, the usage of modern JavaScript and libraries
like react is imminent. The goal of this tooling is to:

-   ✅ Provide out of the box compiling and bundling of all front-end assets.
-   ✅ Give best in class Developer Experience (DX).
    -   Hot Module Replacement and Live Reload.
    -   Compile files on save.
    -   Work on any local development server.
-   ✅ Support modern and useful concepts like modules, tree-shaking, dynamic import etc.

and eliminate the pain points such as:

-   ❌ Boilerplate for setting up your project.
-   ❌ Doing a lot of configuration to setup webpack.
-   ❌ A lot of things to hook webpack with browsersync. We can not safely have webpack dev server because it doesn't reload for PHP files.
-   ❌ A lot of dependencies like babel, webpack loaders and what not.

## What is supported out of the box

-   👉 Have Create React App like developer experience for WordPress Plugin/Theme development.
-   👉 Consume all the modern packages from [npm registry](https://npmjs.com).
-   👉 Write javascript with modern ES2018 (ES6+) syntax and compile it down to ES5 (or in accordance to your `.browserslistrc`).
-   👉 Automatically minify and bundle code with [webpack](https://webpack.js.org).
-   👉 Split large files automatically and have PHP library to `wp_enqueue_script` all generated parts.
-   👉 Use SASS/SCSS language to create stylesheets.
-   👉 Use postcss autoprefixer to automatically make your CSS work with needed vendor prefixes.
-   👉 Implement all the above to your existing wamp, mamp, vvv (basically any) dev server.
-   👉 Create production grade, super optimized and minified files with one command (hello CI).

Here are a few more bonus you get for using wpackio.

-   😎 Using [ES6 Modules](https://scrimba.com/p/p4Mrt9/c9kMkhM) you will never run into namespace collision.
    > Remember when that third-party plugin was using that old version of `foo` library which caused
    > your system to completely fail? No more!.
-   😎 Zero configuration for a sane default of all the toolings involved (babel, sass, webpack).
-   😎 Your CSS/SCSS changes will reflect instantly.
-   😎 [Typescript](https://www.typescriptlang.org/) and [Flowtype](https://flow.org/) to take your js carrier to the next level. This tooling itself is written in typescript 😉.
-   😎 All the stuff you need to start developing using [react](https://reactjs.org/). Hello Gutenberg!

## Getting Started

Everything is documented in our [website](https://wpack.io).

#### TL;DR

-   Add `@wpackio/scripts` to a project by running this.
    ```bash
    npx @wpackio/scripts bootstrap
    ```
-   Edit the `wpackio.project.js` file to write your javascript entrypoints.
-   Use `wpackio/enqueue` from [composer](https://packagist.org/packages/wpackio/enqueue) to consume the assets.
-   Start the server using `npm start`.
-   Create production file using `npm run build`.

## How wpack.io solves the problems?

Behind the scene wpack.io uses [webpack](https://webpack.js.org/) along with
[browsersync](https://browsersync.io/).

It doesn't concern itself with providing boilerplate or starter templates. It
assumes that **you** (the awesome developer `👨‍💻 || 👩‍💻`) is already doing that and what you
want is a simple to configure, yet hackable to the core tooling for bundling
all your frontend assets (js, css, images, svgs) in the most optimized way and
make it work within your WordPress theme or plugin.

Keeping that in mind, wpack.io provides two dependencies for your projects:

1. `@wpackio/scripts` - As main dependency of your `package.json`.
2. `wpackio/enqueue` - As main dependency of your `composer.json`.

The first handles all the tasks for building the assets and providing a damn
good DX.

The second handles enqueuing the assets using WordPress' API (`wp_enqueue_script`
and `wp_enqueue_style`).

Both the tools communicate with each other through the means of `manifest.json`
file. The first tell the later which files to consume and the later `publicPath`
to the first.

## See it in action

We have examples inside [examples](./examples) directory of this repo. Each of
them has intructions in the readme file, so be sure to check out.

### `npx @wpackio/scripts bootstrap`

Bootstrap wpack.io into any existing or new project. This command has to be run
from within the project.

<p align="center">
  <img src="https://raw.githubusercontent.com/swashata/wp-webpack-script/master/assets/bootstrap.gif">
</p>

### `npm start`

After configuring all entrypoints and using the PHP library for consuming, we
start the development server.

<p align="center">
  <img src="https://raw.githubusercontent.com/swashata/wp-webpack-script/master/assets/start.gif">
</p>

Once done, we press <kbd>Ctrl</kbd> + <kbd>c</kbd> to stop it.

<p align="center">
  <img src="https://raw.githubusercontent.com/swashata/wp-webpack-script/master/assets/stop.gif">
</p>

### `npm run build`

Now we create production build.

<p align="center">
  <img src="https://raw.githubusercontent.com/swashata/wp-webpack-script/master/assets/build.gif">
</p>

## Learn more

This Readme is not an extensive source of documentation. Please visit our website
[wpack.io](https://wpack.io) to learn more.

## Contributing

Well thank you ❤️. Please read [Contributing Guide](./CONTRIBUTION.md).
