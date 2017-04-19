# npmdoc-levelgraph

#### api documentation for  [levelgraph (v2.0.1)](https://github.com/mcollina/levelgraph#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-levelgraph.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-levelgraph) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-levelgraph.svg)](https://travis-ci.org/npmdoc/node-npmdoc-levelgraph)

#### A graph database for Node.js and the browser built on top of LevelUp

[![NPM](https://nodei.co/npm/levelgraph.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/levelgraph)

- [https://npmdoc.github.io/node-npmdoc-levelgraph/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-levelgraph/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-levelgraph/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matteo Collina"
    },
    "bugs": {
        "url": "http://github.com/mcollina/levelgraph/issues"
    },
    "dependencies": {
        "callback-stream": "^1.1.0",
        "inherits": "^2.0.1",
        "level-ws": "0.0.1",
        "lodash.keys": "^4.0.6",
        "pump": "^1.0.1",
        "readable-stream": "^2.0.0",
        "steed": "^1.1.3",
        "xtend": "~4.0.0"
    },
    "description": "A graph database for Node.js and the browser built on top of LevelUp",
    "devDependencies": {
        "browserify": "^13.0.1",
        "chai": "^3.5.0",
        "coveralls": "^2.11.2",
        "istanbul": "~0.4.3",
        "jshint": "^2.9.2",
        "level-browserify": "^1.0.1",
        "level-sublevel": "^6.4.6",
        "memdb": "^1.3.1",
        "mocha": "^3.0.0",
        "multilevel": "^7.2.0",
        "osenv": "^0.1.0",
        "pre-commit": "^1.1.3",
        "setimmediate": "^1.0.2",
        "sinon": "~1.17.4",
        "sinon-chai": "^2.6.0",
        "uglify-js": "^2.6.2",
        "zuul": "^3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "dec1caa4d997dac9641244f99f6886c271003256",
        "tarball": "https://registry.npmjs.org/levelgraph/-/levelgraph-2.0.1.tgz"
    },
    "gitHead": "8d57034e84a7fef89267100bad66a85a4256dc74",
    "homepage": "https://github.com/mcollina/levelgraph#readme",
    "keywords": [
        "leveldb",
        "graph",
        "level",
        "database",
        "triples",
        "triple"
    ],
    "license": "MIT",
    "main": "lib/levelgraph.js",
    "maintainers": [
        {
            "name": "matteo.collina"
        }
    ],
    "name": "levelgraph",
    "optionalDependencies": {},
    "pre-commit": [
        "jshint-lib",
        "jshint-test",
        "test"
    ],
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mcollina/levelgraph.git"
    },
    "scripts": {
        "ci": "mocha --recursive --bail --watch test",
        "coverage": "rm -rf coverage; istanbul cover _mocha -- --recursive --reporter spec --bail",
        "jshint-lib": "jshint lib/*.js",
        "jshint-test": "jshint test/*.js",
        "publish-coverage": "cat coverage/lcov.info | coveralls",
        "test": "mocha --recursive --bail --reporter spec test",
        "zuul": "zuul test/common.js test/*spec.js",
        "zuul-local": "zuul --open --local 8080 -- test/common.js test/*spec.js"
    },
    "version": "2.0.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
