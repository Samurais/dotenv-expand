# dotenv-expand

<img src="https://raw.githubusercontent.com/motdotla/dotenv-expand/master/dotenv-expand.png" alt="dotenv-expand" align="right" />

Dotenv-expand adds variable expansion on top of 
[dotenv](http://github.com/motdotla/dotenv). If you find yourself needing to
expand environment variables already existing on your machine, then
dotenv-expand is your tool.

[![BuildStatus](https://img.shields.io/travis/motdotla/dotenv-expand/master.svg?style=flat-square)](https://travis-ci.org/motdotla/dotenv-expand)
[![NPM version](https://img.shields.io/npm/v/dotenv-expand.svg?style=flat-square)](https://www.npmjs.com/package/dotenv-expand)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/feross/standard)

## Install

```bash
npm install @chatopera/dotenv --save
```

## Usage

Define vars in .env

```
OTHER_ENV=foo
YOUR_ENV_VAR=$OTHER_ENV/bar
```

As early as possible in your application, require dotenv and dotenv-expand, and
wrap dotenv expand around dotenv.

```js
require('@chatopera/dotenv').config(process.cwd() + '/.env')
process.env["YOUR_ENV_VAR"]
```

See [test/.env](./test/.env) for examples of variable expansion in your `.env`
file. 

