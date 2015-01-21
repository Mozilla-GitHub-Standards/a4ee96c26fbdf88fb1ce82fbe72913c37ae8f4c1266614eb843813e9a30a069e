# node-firefox-build-tools

Common build tasks and configuration files for the
[node-firefox project](https://github.com/mozilla/node-firefox/).

[![Install with NPM](https://nodei.co/npm/node-firefox-build-tools.png?downloads=true&stars=true)](https://nodei.co/npm/node-firefox-build-tools/)

Right now this is just a set of common gulp tasks and style checks.

## Usage

Install first: `npm install --save-dev node-firefox-build-tools`.

If you are not using gulp in your module yet, now is the right time to add it:

```bash
npm install --save-dev gulp
```

Then either create a `gulpfile.js` or edit the existing one to start using the build tools:

```javascript
var gulp = require('gulp');
var buildTools = require('node-firefox-build-tools');

buildTools.loadGulpTasks(gulp);
```

## Available tasks

#### `lint`

> Run quality and style checks on your code.

#### `nodeunit`

> Run all nodeunit tests matching `tests/unit/**/test.*.js`

#### `test`

> Run linters and tests. You may want to override this task.

#### `watch`

> Run linters and tests whenever code is updated. This is handy if you want
  instant feedback on code you write! (_This is the default task._)

## Bootstrap for new node-firefox modules

You can use the included `node-firefox-init-project` binary to copy our
up-to-date Gulpfile and TravisCI files into your project. This means even less
work when you create a new `node-firefox` module:

```sh
cd node-firefox-something-something # go to your project on the command line
node-firefox-init-project # create your files; you're finished!
```

## License

This program is free software; it is distributed under an
[Apache License](https://github.com/mozilla/node-firefox-build-tools/blob/master/LICENSE).

## Copyright

Copyright (c) 2015 [Mozilla](https://mozilla.org)
([Contributors](https://github.com/mozilla/node-firefox-build-tools/graphs/contributors)).
