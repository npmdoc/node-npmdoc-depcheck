# api documentation for  [depcheck (v0.6.7)](https://github.com/depcheck/depcheck#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-depcheck.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-depcheck) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-depcheck.svg)](https://travis-ci.org/npmdoc/node-npmdoc-depcheck)
#### Check dependencies in your node module

[![NPM](https://nodei.co/npm/depcheck.png?downloads=true)](https://www.npmjs.com/package/depcheck)

[![apidoc](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-depcheck_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-depcheck/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-depcheck/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Djordje Lukic",
        "email": "lukic.djordje@gmail.com"
    },
    "bin": {
        "depcheck": "bin/depcheck"
    },
    "bugs": {
        "url": "https://github.com/depcheck/depcheck/issues"
    },
    "contributors": [
        {
            "name": "Junle Li",
            "email": "lijunle@gmail.com"
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
            "name": "lijunle",
            "email": "lijunle@gmail.com"
        },
        {
            "name": "rumpl",
            "email": "lukic.djordje@gmail.com"
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
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module depcheck](#apidoc.module.depcheck)
1.  object <span class="apidocSignatureSpan">depcheck.</span>detector
1.  object <span class="apidocSignatureSpan">depcheck.</span>parser
1.  object <span class="apidocSignatureSpan">depcheck.</span>special

#### [module depcheck.detector](#apidoc.module.depcheck.detector)
1.  [function <span class="apidocSignatureSpan">depcheck.detector.</span>gruntLoadTaskCallExpression (node)](#apidoc.element.depcheck.detector.gruntLoadTaskCallExpression)
1.  [function <span class="apidocSignatureSpan">depcheck.detector.</span>importDeclaration (node)](#apidoc.element.depcheck.detector.importDeclaration)
1.  [function <span class="apidocSignatureSpan">depcheck.detector.</span>requireCallExpression (node)](#apidoc.element.depcheck.detector.requireCallExpression)

#### [module depcheck.parser](#apidoc.module.depcheck.parser)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>coffee (content)](#apidoc.element.depcheck.parser.coffee)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>es6 (content)](#apidoc.element.depcheck.parser.es6)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>es7 (content)](#apidoc.element.depcheck.parser.es7)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>jsx (content)](#apidoc.element.depcheck.parser.jsx)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>sass (content, filePath, deps, rootDir)](#apidoc.element.depcheck.parser.sass)
1.  [function <span class="apidocSignatureSpan">depcheck.parser.</span>typescript (content, filePath)](#apidoc.element.depcheck.parser.typescript)

#### [module depcheck.special](#apidoc.module.depcheck.special)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>babel (content, filePath, deps)](#apidoc.element.depcheck.special.babel)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>bin (content, filepath, deps, dir)](#apidoc.element.depcheck.special.bin)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>commitizen (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.commitizen)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>eslint (content, filename, deps, rootDir)](#apidoc.element.depcheck.special.eslint)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>feross-standard (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.feross-standard)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>gulp-load-plugins (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.gulp-load-plugins)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>mocha (content, filepath, deps, rootDir)](#apidoc.element.depcheck.special.mocha)
1.  [function <span class="apidocSignatureSpan">depcheck.special.</span>webpack (content, filepath, deps)](#apidoc.element.depcheck.special.webpack)



# <a name="apidoc.module.depcheck"></a>[module depcheck](#apidoc.module.depcheck)



# <a name="apidoc.module.depcheck.detector"></a>[module depcheck.detector](#apidoc.module.depcheck.detector)

#### <a name="apidoc.element.depcheck.detector.gruntLoadTaskCallExpression"></a>[function <span class="apidocSignatureSpan">depcheck.detector.</span>gruntLoadTaskCallExpression (node)](#apidoc.element.depcheck.detector.gruntLoadTaskCallExpression)
- description and source-code
```javascript
function detectGruntLoadTaskCallExpression(node) {
  return node.type === 'CallExpression' && node.callee && node.callee.property && node.callee.property.name === 'loadNpmTasks' &&
node.arguments[0] ? [node.arguments[0].value] : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.detector.importDeclaration"></a>[function <span class="apidocSignatureSpan">depcheck.detector.</span>importDeclaration (node)](#apidoc.element.depcheck.detector.importDeclaration)
- description and source-code
```javascript
function detectImportDeclaration(node) {
  return node.type === 'ImportDeclaration' && node.source && node.source.value ? [node.source.value] : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.detector.requireCallExpression"></a>[function <span class="apidocSignatureSpan">depcheck.detector.</span>requireCallExpression (node)](#apidoc.element.depcheck.detector.requireCallExpression)
- description and source-code
```javascript
function detectRequireCallExpression(node) {
  return node.type === 'CallExpression' && node.callee && node.callee.type === 'Identifier' && node.callee.name === 'require' &&
node.arguments[0] && _lodash2.default.isString(node.arguments[0].value) ? [node.arguments[0].value] : [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.depcheck.parser"></a>[module depcheck.parser](#apidoc.module.depcheck.parser)

#### <a name="apidoc.element.depcheck.parser.coffee"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>coffee (content)](#apidoc.element.depcheck.parser.coffee)
- description and source-code
```javascript
function parseCoffeeScript(content) {
  return re.getDependencies(content);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.parser.es6"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>es6 (content)](#apidoc.element.depcheck.parser.es6)
- description and source-code
```javascript
function parseES6(content) {
  return (0, _babylon.parse)(content, {
    sourceType: 'module'
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.parser.es7"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>es7 (content)](#apidoc.element.depcheck.parser.es7)
- description and source-code
```javascript
function parseES7(content) {
  return (0, _babylon.parse)(content, {
    sourceType: 'module',

    // Enable all possible babylon plugins.
    // Because we only parse them, not evaluate any code, it is safe to do so.
    plugins: ['*']
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.parser.jsx"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>jsx (content)](#apidoc.element.depcheck.parser.jsx)
- description and source-code
```javascript
function parseJSX(content) {
  return (0, _babylon.parse)(content, {
    sourceType: 'module',

    // Enable all possible babylon plugins.
    // Because the guys using React always want the newest syntax.
    plugins: ['*', 'jsx']
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.parser.sass"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>sass (content, filePath, deps, rootDir)](#apidoc.element.depcheck.parser.sass)
- description and source-code
```javascript
function parseSASS(content, filePath, deps, rootDir) {
  var _sass$renderSync = sass.renderSync({
    data: content,
    includePaths: [_path2.default.dirname(filePath)]
  }),
      stats = _sass$renderSync.stats;

  var result = (0, _lodash2.default)(stats.includedFiles).map(function (file) {
    return _path2.default.relative(rootDir, file);
  }).filter(function (file) {
    return file.indexOf('node_modules') === 0;
  }) // refer to node_modules
  .map(function (file) {
    return file.replace(/\\/g, '/');
  }) // normalize paths in Windows
  .map(function (file) {
    return file.substring('node_modules/'.length);
  }) // avoid heading slash
  .map(_requirePackageName2.default).uniq().value();

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.parser.typescript"></a>[function <span class="apidocSignatureSpan">depcheck.parser.</span>typescript (content, filePath)](#apidoc.element.depcheck.parser.typescript)
- description and source-code
```javascript
function parseTypescript(content, filePath) {
  if (!typescript) {
    return [];
  }

  var compileOptions = {
    module: typescript.ModuleKind.CommonJS,
    target: typescript.ScriptTarget.Latest
  };

  var result = typescript.transpile(content, compileOptions, filePath);

  // TODO avoid parse source file twice, use Typescript native traverser to find out dependencies.
  // Reference: https://github.com/Microsoft/TypeScript/wiki/Using-the-Compiler-API#traversing-the-ast-with-a-little-linter
  return (0, _babylon.parse)(result, {
    sourceType: 'module'
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.depcheck.special"></a>[module depcheck.special](#apidoc.module.depcheck.special)

#### <a name="apidoc.element.depcheck.special.babel"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>babel (content, filePath, deps)](#apidoc.element.depcheck.special.babel)
- description and source-code
```javascript
function parseBabel(content, filePath, deps) {
  var filename = _path2.default.basename(filePath);

  if (filename === '.babelrc') {
    var options = parse(content);
    return checkOptions(deps, options);
  }

  if (filename === 'package.json') {
    var metadata = parse(content);
    return checkOptions(deps, metadata.babel);
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.bin"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>bin (content, filepath, deps, dir)](#apidoc.element.depcheck.special.bin)
- description and source-code
```javascript
function parseBinary(content, filepath, deps, dir) {
  var scripts = (0, _utils.getScripts)(filepath, content);
  return deps.filter(function (dep) {
    return isBinaryInUse(dep, scripts, dir);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.commitizen"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>commitizen (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.commitizen)
- description and source-code
```javascript
function parseCommitizen(content, filePath, deps, rootDir) {
  var packageJsonPath = _path2.default.resolve(rootDir, 'package.json');
  var resolvedFilePath = _path2.default.resolve(filePath);

  if (resolvedFilePath === packageJsonPath) {
    var metadata = JSON.parse(content);

    if (metadata.config && metadata.config.commitizen && metadata.config.commitizen.path) {
      var commitizenPath = metadata.config.commitizen.path;

      if (!commitizenPath.startsWith('.')) {
        return [(0, _requirePackageName2.default)(commitizenPath)];
      }

      var normalizedPath = _path2.default.normalize(commitizenPath).replace(/\\/g, '/');

      if (!normalizedPath.startsWith('node_modules')) {
        // The path is not refering to a file in another module
        return [];
      }

      var packagePath = normalizedPath.substring('node_modules/'.length);

      return [(0, _requirePackageName2.default)(packagePath)];
    }
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.eslint"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>eslint (content, filename, deps, rootDir)](#apidoc.element.depcheck.special.eslint)
- description and source-code
```javascript
function parseESLint(content, filename, deps, rootDir) {
  var basename = _path2.default.basename(filename);
  if (/^\.eslintrc(\.json|\.js|\.yml|\.yaml)?$/.test(basename)) {
    var config = parse(content);
    return checkConfig(config, rootDir);
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.feross-standard"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>feross-standard (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.feross-standard)
- description and source-code
```javascript
function parseFerossStandard(content, filePath, deps, rootDir) {
  var packageJsonPath = _path2.default.resolve(rootDir, 'package.json');
  var resolvedFilePath = _path2.default.resolve(filePath);
  if (resolvedFilePath === packageJsonPath && deps.indexOf('standard') !== -1) {
    var metadata = JSON.parse(content);
    var config = metadata.standard || {};
    var parser = config.parser;
    return parser ? [parser] : [];
  }

  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.gulp-load-plugins"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>gulp-load-plugins (content, filePath, deps, rootDir)](#apidoc.element.depcheck.special.gulp-load-plugins)
- description and source-code
```javascript
function parseGulpPlugins(content, filePath, deps, rootDir) {
  var resolvedPath = (0, _path.resolve)(filePath);
  if (resolvedPath !== (0, _path.resolve)(rootDir, 'gulpfile.js') && resolvedPath !== (0, _path.resolve)(rootDir, 'gulpfile.babel
.js')) {
    return [];
  }

  var pluginLookup = getPluginLookup(deps);
  var ast = (0, _es2.default)(content);
  var results = [];
  (0, _babelTraverse2.default)(ast, {
    enter: function enter(path) {
      results.push.apply(results, _toConsumableArray(check(content, pluginLookup, path)));
    }
  });

  return (0, _lodash2.default)(results).filter().uniq().value();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.mocha"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>mocha (content, filepath, deps, rootDir)](#apidoc.element.depcheck.special.mocha)
- description and source-code
```javascript
function parseMocha(content, filepath, deps, rootDir) {
  var defaultOptPath = _path2.default.resolve(rootDir, 'test/mocha.opts');
  if (filepath === defaultOptPath) {
    return getRequires(content, deps);
  }

  // get mocha.opts from scripts
  var requires = (0, _lodash2.default)((0, _utils.getScripts)(filepath, content)).filter(function (script) {
    return script.indexOf('mocha') !== -1;
  }).map(function (script) {
    return getOpts(script);
  }).filter(function (opts) {
    return opts;
  }).map(function (opts) {
    return _path2.default.resolve(filepath, '..', opts);
  }).map(function (optPath) {
    return _fs2.default.readFileSync(optPath, 'utf-8');
  }) // TODO async read file
  .map(function (optContent) {
    return getRequires(optContent, deps);
  }).flatten().value();

  return requires;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.depcheck.special.webpack"></a>[function <span class="apidocSignatureSpan">depcheck.special.</span>webpack (content, filepath, deps)](#apidoc.element.depcheck.special.webpack)
- description and source-code
```javascript
function parseWebpack(content, filepath, deps) {
  var filename = _path2.default.basename(filepath);
  if (webpackConfigRegex.test(filename)) {
    var module = require(filepath).module || {}; // eslint-disable-line global-require
    var loaders = getLoaders(deps, module.loaders);
    var preLoaders = getLoaders(deps, module.preLoaders);
    var postLoaders = getLoaders(deps, module.postLoaders);
    return loaders.concat(preLoaders).concat(postLoaders);
  }

  return [];
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
