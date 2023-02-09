# ts-lib-boilerplate

This is a simple boilerplate for a Typescript project meant to be used as a starting point for my library projects.

It's based on the setup described in [this](https://www.youtube.com/watch?v=vRmLTZyq57U) video.

Includes:
- Setup for Typescript build to ES5 and ES6.
- Support for installation as library from git.
- Testing with jest and ts-jest.

## Todo

- Add dist/package.json for distribution on NPM.

## Installing from git

The boilerplate supports installing from git, and will automatically build the library.

After:

> npm install -S \<repo-url>

The `prepare` script will be run by npm and build the library.

After that, `dist/es5/index.js` and `dist/es6/index.js` will be served as CommonJS or ES6 modules respectively:

> import { hello } from 'ts-lib-boilerplate'; // ES6  

> const hello = require('ts-lib-boilerplate'); // CommonJS

**NOTE:** The empty .npmignore is necessary for this to work; if it's missing, npm will ignore the dist folder (because it's in the .gitignore file) and won't generate it correctly on installation.