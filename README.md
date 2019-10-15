# Preact TypeScript-Sass starter project

## Documentation

-   This is a TypeScript + Sass version of the default template for
    [preact-cli](https://github.com/developit/preact-cli).
-   [For Preact](https://preactjs.com/): General information about how to work
    with Preact, not specific to this template
-   Interested in automated boilerplate generation for components and routes for your Preact X projects? Check out this awesome cli at https://github.com/IntuitiveInformatics/preact-custom-cli

## Usage

```bash
$ npm install -g preact-cli
$ preact create thomashuangcn/ts-sass my-project
$ cd my-project
$ npm install
$ npm run dev
```

Development server runs on port `8080`. If the default port is already in use on
your machine it will start the development server on a random port.

### Sass Usage

When you run `npm run dev` or `npm run serve`, the "typed-scss-module" library will automatically watch 
your stylesheets with the `.scss` extension and generate the appropriate declarations files for them.
However, a declarations file will only be generated when the stylesheet contains at least one
class-based or id-based declaration block with valid declarations as the block content.

When you run `npm run build`, the "typed-scss-module" library will run exactly once to ensure that 
all `.scss` stylesheets have appropriate declaration files before production build.

You may also run `npx tsm src` in the root directory of the project to manually generate declaration 
files without watching the stylesheets. Use `npx tsm src -w` to watch the stylesheets manually.

## Commands

-   `npm run start`: Runs `serve` or `dev`, depending on `NODE_ENV` value.
    Defaults to `dev server`

-   `npm run dev`: Run a development, HMR server

-   `npm run serve`: Run a production-like server

-   `npm run build`: Production-ready build

-   `npm run lint`: Pass TypeScript files using TSLint

-   `npm run test`: Run Jest and
    [`preact-render-spy`](https://github.com/mzgoddard/preact-render-spy) for
    your tests

### How to Test

The `ts-sass` template provides a basic test setup with Jest and
[`preact-render-spy`](https://github.com/mzgoddard/preact-render-spy). You are
free to change preact-render-spy with any other assertion library. The advantage
of it is that it supports a similiar terminology and feature set as the Enzyme
library for testing React applications.

You can run all additional Jest CLI commands with the `npm run test` command as
described in the
[Jest docs](https://facebook.github.io/jest/docs/en/cli.html#using-with-npm-scripts).
For example, running jest in watch mode would be :

-   `npm run test -- --watch` instead of `jest --watch`
