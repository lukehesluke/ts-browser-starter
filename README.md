# ts-browser-starter

Fairly minimal browser TypeScript starter project. It contains:

- NVM is set to node LTS (at time of writing)
- TSConfig includes strict mode and is otherwise fairly standard
- ESLint with standard settings
- Prettier with standard settings and set to be used by VSCode for formatting
- Webpack and SWC for building TypeScript files -> JavaScript
  - It uses content hashing so that changes can be seen when refreshing the page in a caching browser
- html-webpack-plugin is used to build a minimal HTML page which calls the built JavaScript files
- React.js with `.tsx` files **in the [`with-react`](../../tree/with-react) branch**.

That's it. Bye 🦧

## Using this Starter Project

1. `git clone` this project
2. Replace the git repo with `rm -rf .git && git init`
3. Update `.name` and `.description` in `package.json`
4. Update `.title` in the `HtmlWebpackPlugin` args in `webpack.config.js`
5. Rename "YOUR PROJECT" in the next section
6. Remove this first section of the README.md
7. hav fun 🍌

## How it was made

1. Following this guide for enabling ESLint and Prettier in a TypeScript project:
   1. https://khalilstemmler.com/blogs/tooling/prettier/
2. And then configuring `tsconfig.json` to enable lots of features (e.g. `downLevelIteration`) and to use `strict` mode.

# YOUR PROJECT

## Set-up

```sh
nvm use # Pre-requisite: Have NVM
npm install
```

## Running

```sh
npm run build
npm run serve
```

## Running (dev commands)

- In one terminal, build and watch for changes: `npm run build:watch`
- In another terminal, serve the app to `http://localhost:8080` with `npm run serve`

## Testing

```sh
npm test
```

This checks for errors with ESLint, Prettier and TypeScript Compiler.

**Note** that building uses SWC, rather than TypeScript Compiler and so does not find type errors.
