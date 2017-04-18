# npmdoc-depcheck

#### api documentation for  [depcheck (v0.6.7)](https://github.com/depcheck/depcheck#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-depcheck.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-depcheck) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-depcheck.svg)](https://travis-ci.org/npmdoc/node-npmdoc-depcheck)

#### Check dependencies in your node module

[![NPM](https://nodei.co/npm/depcheck.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/depcheck)

- [https://npmdoc.github.io/node-npmdoc-depcheck/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-depcheck/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-depcheck/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Djordje Lukic"
    },
    "bin": {
        "depcheck": "bin/depcheck"
    },
    "bugs": {
        "url": "https://github.com/depcheck/depcheck/issues"
    },
    "contributors": [
        {
            "name": "Junle Li"
        }
    ],
    "dependencies": {
        "babel-traverse": "^6.7.3",
        "babylon": "^6.1.21",
        "builtin-modules": "^1.1.1",
        "deprecate": "^1.0.0",
        "deps-regex": "^0.1.4",
        "js-yaml": "^3.4.2",
        "lodash": "^4.5.1",
        "minimatch": "^3.0.2",
        "require-package-name": "^2.0.1",
        "walkdir": "0.0.11",
        "yargs": "^6.0.0"
    },
    "description": "Check dependencies in your node module",
    "devDependencies": {
        "babel-cli": "^6.1.1",
        "babel-eslint": "^7.0.0",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-plugin-istanbul": "^3.0.0",
        "babel-plugin-transform-object-assign": "^6.1.18",
        "babel-polyfill": "^6.16.0",
        "babel-preset-es2015": "^6.0.15",
        "babel-preset-stage-2": "^6.0.15",
        "babel-register": "^6.18.0",
        "codecov.io": "^0.1.6",
        "cross-env": "^3.1.3",
        "depcheck-web": "^0.1.0",
        "dependent-build": "^0.1.2",
        "eslint": "^3.10.1",
        "eslint-config-airbnb": "^13.0.0",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-jsx-a11y": "^2.2.3",
        "eslint-plugin-react": "^6.7.0",
        "fs-promise": "^1.0.0",
        "mocha": "^3.0.0",
        "node-sass": "^3.4.0",
        "node-version-check": "^2.1.1",
        "nyc": "^10.0.0",
        "patch-version": "^0.1.1",
        "should": "^11.0.0",
        "typescript": "^1.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "6b3d1e993931e09ee673d3507d3175db734823e6",
        "tarball": "https://registry.npmjs.org/depcheck/-/depcheck-0.6.7.tgz"
    },
    "engines": {
        "node": ">=0.12"
    },
    "gitHead": "083e5d72bd0b26be3240a9850ccab1103228087e",
    "homepage": "https://github.com/depcheck/depcheck#readme",
    "keywords": [
        "check",
        "unused",
        "package",
        "packages",
        "depcheck",
        "dependency",
        "dependencies",
        "devDependencies"
    ],
    "license": "MIT",
    "main": "dist/index.js",
    "maintainers": [
        {
            "name": "lijunle"
        },
        {
            "name": "rumpl"
        }
    ],
    "name": "depcheck",
    "nyc": {
        "sourceMap": false,
        "instrument": false,
        "exclude": [
            "dist",
            "test"
        ],
        "require": [
            "babel-polyfill",
            "babel-register"
        ],
        "reporter": [
            "html",
            "text"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/depcheck/depcheck.git"
    },
    "scripts": {
        "compile": "babel src/ -d dist/",
        "component": "babel-node ./build/component.js > ./dist/component.json",
        "depcheck": "node ./bin/depcheck",
        "depcheck-json": "node ./bin/depcheck --json | babel-node ./build/check-json",
        "depcheck-web": "node ./bin/depcheck --json | depcheck-web",
        "lint": "node-version-gte-4 && eslint ./src ./test ./build || node-version-lt-4",
        "prepublish": "npm run compile && npm run component",
        "test": "babel-node node_modules/mocha/bin/_mocha ./test ./test/special --timeout 10000",
        "test-coverage": "babel-node node_modules/cross-env/bin/cross-env.js NODE_ENV=test nyc mocha ./test ./test/special --timeout 20000 && nyc report --reporter=text-lcov > ./coverage/coverage.lcov",
        "test-dependent": "node-version-gte-4 && dependent-build || node-version-lt-4"
    },
    "version": "0.6.7"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
