# api documentation for  [levelgraph (v2.0.1)](https://github.com/mcollina/levelgraph#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-levelgraph.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-levelgraph) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-levelgraph.svg)](https://travis-ci.org/npmdoc/node-npmdoc-levelgraph)
#### A graph database for Node.js and the browser built on top of LevelUp

[![NPM](https://nodei.co/npm/levelgraph.png?downloads=true)](https://www.npmjs.com/package/levelgraph)

[![apidoc](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-levelgraph_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-levelgraph/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-levelgraph/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matteo Collina",
        "email": "hello@matteocollina.com"
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
            "name": "matteo.collina",
            "email": "hello@matteocollina.com"
        }
    ],
    "name": "levelgraph",
    "optionalDependencies": {},
    "pre-commit": [
        "jshint-lib",
        "jshint-test",
        "test"
    ],
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module levelgraph](#apidoc.module.levelgraph)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>filterstream (options)](#apidoc.element.levelgraph.filterstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>joinstream (options)](#apidoc.element.levelgraph.joinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>materializerstream (options)](#apidoc.element.levelgraph.materializerstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>navigator (options)](#apidoc.element.levelgraph.navigator)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>sortjoinstream (options)](#apidoc.element.levelgraph.sortjoinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>variable (name)](#apidoc.element.levelgraph.variable)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>writestream (options)](#apidoc.element.levelgraph.writestream)
1.  object <span class="apidocSignatureSpan">levelgraph.</span>filterstream.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>joinstream.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>materializerstream.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>navigator.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>sortjoinstream.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>utilities
1.  object <span class="apidocSignatureSpan">levelgraph.</span>variable.prototype
1.  object <span class="apidocSignatureSpan">levelgraph.</span>writestream.prototype

#### [module levelgraph.filterstream](#apidoc.module.levelgraph.filterstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>filterstream (options)](#apidoc.element.levelgraph.filterstream.filterstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.filterstream.</span>super_ (options)](#apidoc.element.levelgraph.filterstream.super_)

#### [module levelgraph.filterstream.prototype](#apidoc.module.levelgraph.filterstream.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.filterstream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.filterstream.prototype._transform)
1.  [function <span class="apidocSignatureSpan">levelgraph.filterstream.prototype.</span>destroy ()](#apidoc.element.levelgraph.filterstream.prototype.destroy)

#### [module levelgraph.joinstream](#apidoc.module.levelgraph.joinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>joinstream (options)](#apidoc.element.levelgraph.joinstream.joinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.joinstream.</span>super_ (options)](#apidoc.element.levelgraph.joinstream.super_)

#### [module levelgraph.joinstream.prototype](#apidoc.module.levelgraph.joinstream.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.joinstream.prototype.</span>_transform (solution, encoding, done)](#apidoc.element.levelgraph.joinstream.prototype._transform)

#### [module levelgraph.materializerstream](#apidoc.module.levelgraph.materializerstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>materializerstream (options)](#apidoc.element.levelgraph.materializerstream.materializerstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.materializerstream.</span>super_ (options)](#apidoc.element.levelgraph.materializerstream.super_)

#### [module levelgraph.materializerstream.prototype](#apidoc.module.levelgraph.materializerstream.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.materializerstream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.materializerstream.prototype._transform)

#### [module levelgraph.navigator](#apidoc.module.levelgraph.navigator)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>navigator (options)](#apidoc.element.levelgraph.navigator.navigator)

#### [module levelgraph.navigator.prototype](#apidoc.module.levelgraph.navigator.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>archIn (predicate)](#apidoc.element.levelgraph.navigator.prototype.archIn)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>archOut (predicate)](#apidoc.element.levelgraph.navigator.prototype.archOut)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>as (name)](#apidoc.element.levelgraph.navigator.prototype.as)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>bind (value)](#apidoc.element.levelgraph.navigator.prototype.bind)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>contexts (query, cb)](#apidoc.element.levelgraph.navigator.prototype.contexts)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>contextsStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.contextsStream)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>go (vertex)](#apidoc.element.levelgraph.navigator.prototype.go)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>solutions (query, cb)](#apidoc.element.levelgraph.navigator.prototype.solutions)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>solutionsStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.solutionsStream)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>triples (query, cb)](#apidoc.element.levelgraph.navigator.prototype.triples)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>triplesStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.triplesStream)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>values (cb)](#apidoc.element.levelgraph.navigator.prototype.values)
1.  [function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>valuesStream ()](#apidoc.element.levelgraph.navigator.prototype.valuesStream)

#### [module levelgraph.sortjoinstream](#apidoc.module.levelgraph.sortjoinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>sortjoinstream (options)](#apidoc.element.levelgraph.sortjoinstream.sortjoinstream)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.</span>super_ (options)](#apidoc.element.levelgraph.sortjoinstream.super_)

#### [module levelgraph.sortjoinstream.prototype](#apidoc.module.levelgraph.sortjoinstream.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_doRead (triple)](#apidoc.element.levelgraph.sortjoinstream.prototype._doRead)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_execLastDone ()](#apidoc.element.levelgraph.sortjoinstream.prototype._execLastDone)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_flush (cb)](#apidoc.element.levelgraph.sortjoinstream.prototype._flush)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_nextTriple (skip)](#apidoc.element.levelgraph.sortjoinstream.prototype._nextTriple)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_start ()](#apidoc.element.levelgraph.sortjoinstream.prototype._start)
1.  [function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_transform (solution, encoding, done)](#apidoc.element.levelgraph.sortjoinstream.prototype._transform)

#### [module levelgraph.utilities](#apidoc.module.levelgraph.utilities)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>createQuery (pattern, options)](#apidoc.element.levelgraph.utilities.createQuery)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>escape (value)](#apidoc.element.levelgraph.utilities.escape)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>findIndex (types, preferiteIndex)](#apidoc.element.levelgraph.utilities.findIndex)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>genKey (key, triple)](#apidoc.element.levelgraph.utilities.genKey)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>genKeys (triple)](#apidoc.element.levelgraph.utilities.genKeys)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>generateBatch (triple, action)](#apidoc.element.levelgraph.utilities.generateBatch)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>maskUpdater (pattern)](#apidoc.element.levelgraph.utilities.maskUpdater)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>matcher (pattern)](#apidoc.element.levelgraph.utilities.matcher)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>materializer (pattern, data)](#apidoc.element.levelgraph.utilities.materializer)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>possibleIndexes (types)](#apidoc.element.levelgraph.utilities.possibleIndexes)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>queryMask (object)](#apidoc.element.levelgraph.utilities.queryMask)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>variablesMask (object)](#apidoc.element.levelgraph.utilities.variablesMask)
1.  [function <span class="apidocSignatureSpan">levelgraph.utilities.</span>wrapCallback (method)](#apidoc.element.levelgraph.utilities.wrapCallback)
1.  object <span class="apidocSignatureSpan">levelgraph.utilities.</span>defs

#### [module levelgraph.variable](#apidoc.module.levelgraph.variable)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>variable (name)](#apidoc.element.levelgraph.variable.variable)

#### [module levelgraph.variable.prototype](#apidoc.module.levelgraph.variable.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>bind (solution, value)](#apidoc.element.levelgraph.variable.prototype.bind)
1.  [function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>isBindable (solution, value)](#apidoc.element.levelgraph.variable.prototype.isBindable)
1.  [function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>isBound (solution)](#apidoc.element.levelgraph.variable.prototype.isBound)

#### [module levelgraph.writestream](#apidoc.module.levelgraph.writestream)
1.  [function <span class="apidocSignatureSpan">levelgraph.</span>writestream (options)](#apidoc.element.levelgraph.writestream.writestream)
1.  [function <span class="apidocSignatureSpan">levelgraph.writestream.</span>super_ (options)](#apidoc.element.levelgraph.writestream.super_)

#### [module levelgraph.writestream.prototype](#apidoc.module.levelgraph.writestream.prototype)
1.  [function <span class="apidocSignatureSpan">levelgraph.writestream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.writestream.prototype._transform)



# <a name="apidoc.module.levelgraph"></a>[module levelgraph](#apidoc.module.levelgraph)

#### <a name="apidoc.element.levelgraph.filterstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>filterstream (options)](#apidoc.element.levelgraph.filterstream)
- description and source-code
```javascript
function FilterStream(options) {
  if (!(this instanceof FilterStream)) {
    return new FilterStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  var that = this;

  this.filter = options.filter;
  this.offset = options.offset;

  this._offsetCounter = 0;

  this._destroyed = false;

  if (this.filter && this.filter.length === 2) {
    this._transform = filterTwoArguments;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.joinstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>joinstream (options)](#apidoc.element.levelgraph.joinstream)
- description and source-code
```javascript
function JoinStream(options) {
  if (!(this instanceof JoinStream)) {
    return new JoinStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.triple = options.triple;
  this.matcher = matcher(options.triple);
  this.mask = queryMask(options.triple);
  this.maskUpdater = maskUpdater(options.triple);
  this.limit = options.limit;
  this._limitCounter = 0;
  this.db = options.db;
  this._index = options.index;
  this._ended = false;

  var that = this;
  this.once('pipe', function(source) {
    source.on('error', function(err) {
      that.emit('error', err);
    });
  });

  this._onDataStream = function onDataStream(triple) {
    var newsolution = that.matcher(that._lastSolution, triple);

    if (that._ended || !newsolution) {
      return;
    }

    that.push(newsolution);

    if (that.limit && ++that._limitCounter === that.limit) {
      that._readStream.destroy();
      that._ended = true;
      that.push(null);
    }
  };

  this._indexPreferences = { index: this._index };

  this._onErrorStream = function onErrorStream(err) {
    that.emit('error', err);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.materializerstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>materializerstream (options)](#apidoc.element.levelgraph.materializerstream)
- description and source-code
```javascript
function MaterializerStream(options) {
  if (!(this instanceof MaterializerStream)) {
    return new MaterializerStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.pattern = options.pattern;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>navigator (options)](#apidoc.element.levelgraph.navigator)
- description and source-code
```javascript
function Navigator(options) {
  if (!(this instanceof Navigator)) {
    return new Navigator(options);
  }

  this.db = options.db;
  this._conditions = [];
  this._initialSolution = {};

  var count = 0;
  this._nextVar = function() {
    return this.db.v('x' + count++);
  };

  this.go(options.start);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.sortjoinstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>sortjoinstream (options)](#apidoc.element.levelgraph.sortjoinstream)
- description and source-code
```javascript
function SortJoinStream(options) {
  if (!(this instanceof SortJoinStream)) {
    return new SortJoinStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.triple = options.triple;
  this.matcher = matcher(options.triple);
  this.db = options.db;

  var that = this;
  this.once('pipe', function(source) {
    source.on('error', function(err) {
      that.emit('error', err);
    });
  });

  this._queryMask = queryMask(options.triple);
  this._queryMask.filter = options.triple.filter;

  this.index = options.index;

  this._previousTriple = null;
  this._lastDone = null;
  this._start();
  this.limit = options.limit;
  this._limitCounter = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.variable"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>variable (name)](#apidoc.element.levelgraph.variable)
- description and source-code
```javascript
function Variable(name) {
  if (!(this instanceof Variable)) {
    return new Variable(name);
  }

  this.name = name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.writestream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>writestream (options)](#apidoc.element.levelgraph.writestream)
- description and source-code
```javascript
function WriteStream(options) {
  if (!(this instanceof WriteStream)) {
    return new WriteStream(options);
  }

  options = options || {};
  options.objectMode = true;

  Transform.call(this, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.filterstream"></a>[module levelgraph.filterstream](#apidoc.module.levelgraph.filterstream)

#### <a name="apidoc.element.levelgraph.filterstream.filterstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>filterstream (options)](#apidoc.element.levelgraph.filterstream.filterstream)
- description and source-code
```javascript
function FilterStream(options) {
  if (!(this instanceof FilterStream)) {
    return new FilterStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  var that = this;

  this.filter = options.filter;
  this.offset = options.offset;

  this._offsetCounter = 0;

  this._destroyed = false;

  if (this.filter && this.filter.length === 2) {
    this._transform = filterTwoArguments;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.filterstream.super_"></a>[function <span class="apidocSignatureSpan">levelgraph.filterstream.</span>super_ (options)](#apidoc.element.levelgraph.filterstream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.filterstream.prototype"></a>[module levelgraph.filterstream.prototype](#apidoc.module.levelgraph.filterstream.prototype)

#### <a name="apidoc.element.levelgraph.filterstream.prototype._transform"></a>[function <span class="apidocSignatureSpan">levelgraph.filterstream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.filterstream.prototype._transform)
- description and source-code
```javascript
function filterOneArgument(data, encoding, done) {

  if ((!this.offset || ++this._offsetCounter > this.offset) &&
      (!this.filter || this.filter(data))) {
    this.push(data);
  }

  done();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.filterstream.prototype.destroy"></a>[function <span class="apidocSignatureSpan">levelgraph.filterstream.prototype.</span>destroy ()](#apidoc.element.levelgraph.filterstream.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  if (!this._destroyed) {
    this.push(null);
  }
  this._destroyed = true;
}
```
- example usage
```shell
...
  if (that._ended || !newsolution) {
    return;
  }

  that.push(newsolution);

  if (that.limit && ++that._limitCounter === that.limit) {
    that._readStream.destroy();
    that._ended = true;
    that.push(null);
  }
};

this._indexPreferences = { index: this._index };
...
```



# <a name="apidoc.module.levelgraph.joinstream"></a>[module levelgraph.joinstream](#apidoc.module.levelgraph.joinstream)

#### <a name="apidoc.element.levelgraph.joinstream.joinstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>joinstream (options)](#apidoc.element.levelgraph.joinstream.joinstream)
- description and source-code
```javascript
function JoinStream(options) {
  if (!(this instanceof JoinStream)) {
    return new JoinStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.triple = options.triple;
  this.matcher = matcher(options.triple);
  this.mask = queryMask(options.triple);
  this.maskUpdater = maskUpdater(options.triple);
  this.limit = options.limit;
  this._limitCounter = 0;
  this.db = options.db;
  this._index = options.index;
  this._ended = false;

  var that = this;
  this.once('pipe', function(source) {
    source.on('error', function(err) {
      that.emit('error', err);
    });
  });

  this._onDataStream = function onDataStream(triple) {
    var newsolution = that.matcher(that._lastSolution, triple);

    if (that._ended || !newsolution) {
      return;
    }

    that.push(newsolution);

    if (that.limit && ++that._limitCounter === that.limit) {
      that._readStream.destroy();
      that._ended = true;
      that.push(null);
    }
  };

  this._indexPreferences = { index: this._index };

  this._onErrorStream = function onErrorStream(err) {
    that.emit('error', err);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.joinstream.super_"></a>[function <span class="apidocSignatureSpan">levelgraph.joinstream.</span>super_ (options)](#apidoc.element.levelgraph.joinstream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.joinstream.prototype"></a>[module levelgraph.joinstream.prototype](#apidoc.module.levelgraph.joinstream.prototype)

#### <a name="apidoc.element.levelgraph.joinstream.prototype._transform"></a>[function <span class="apidocSignatureSpan">levelgraph.joinstream.prototype.</span>_transform (solution, encoding, done)](#apidoc.element.levelgraph.joinstream.prototype._transform)
- description and source-code
```javascript
function transform(solution, encoding, done) {
  if (this._ended) {
    return done();
  }

  var that = this
    , newMask = this.maskUpdater(solution, this.mask);

  that._lastSolution = solution;
  that._readStream = this.db.getStream(newMask, this._indexPreferences);

  that._readStream.on('data', that._onDataStream);
  that._readStream.on('error', that._onErrorStream);
  that._readStream.on('end', done);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.materializerstream"></a>[module levelgraph.materializerstream](#apidoc.module.levelgraph.materializerstream)

#### <a name="apidoc.element.levelgraph.materializerstream.materializerstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>materializerstream (options)](#apidoc.element.levelgraph.materializerstream.materializerstream)
- description and source-code
```javascript
function MaterializerStream(options) {
  if (!(this instanceof MaterializerStream)) {
    return new MaterializerStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.pattern = options.pattern;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.materializerstream.super_"></a>[function <span class="apidocSignatureSpan">levelgraph.materializerstream.</span>super_ (options)](#apidoc.element.levelgraph.materializerstream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.materializerstream.prototype"></a>[module levelgraph.materializerstream.prototype](#apidoc.module.levelgraph.materializerstream.prototype)

#### <a name="apidoc.element.levelgraph.materializerstream.prototype._transform"></a>[function <span class="apidocSignatureSpan">levelgraph.materializerstream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.materializerstream.prototype._transform)
- description and source-code
```javascript
_transform = function (data, encoding, done) {

  this.push(materializer(this.pattern, data));

  done();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.navigator"></a>[module levelgraph.navigator](#apidoc.module.levelgraph.navigator)

#### <a name="apidoc.element.levelgraph.navigator.navigator"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>navigator (options)](#apidoc.element.levelgraph.navigator.navigator)
- description and source-code
```javascript
function Navigator(options) {
  if (!(this instanceof Navigator)) {
    return new Navigator(options);
  }

  this.db = options.db;
  this._conditions = [];
  this._initialSolution = {};

  var count = 0;
  this._nextVar = function() {
    return this.db.v('x' + count++);
  };

  this.go(options.start);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.navigator.prototype"></a>[module levelgraph.navigator.prototype](#apidoc.module.levelgraph.navigator.prototype)

#### <a name="apidoc.element.levelgraph.navigator.prototype.archIn"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>archIn (predicate)](#apidoc.element.levelgraph.navigator.prototype.archIn)
- description and source-code
```javascript
archIn = function (predicate) {
  var triple = {
    predicate: predicate
  };

  triple[varKey] = this._nextVar();
  triple[lastKey] = this._lastElement;

  this._conditions.push(triple);

  this._lastElement = triple[varKey];

  return this;
}
```
- example usage
```shell
...
The Navigator API is a fluent API for LevelGraph, loosely inspired by
[Gremlin](http://markorodriguez.com/2011/06/15/graph-pattern-matching-with-gremlin-1-1/)
It allows to specify how to search our graph in a much more compact way and navigate
between vertexes.

Here is an example, using the same dataset as before:
'''javascript
db.nav("matteo").archIn("friend").archOut("friend").
  solutions(function(err, results) {
  // prints:
  // [ { x0: 'daniele', x1: 'marco' },
  //   { x0: 'daniele', x1: 'matteo' },
  //   { x0: 'lucio', x1: 'marco' },
  //   { x0: 'lucio', x1: 'matteo' } ]
  console.log(results);
...
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.archOut"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>archOut (predicate)](#apidoc.element.levelgraph.navigator.prototype.archOut)
- description and source-code
```javascript
archOut = function (predicate) {
  var triple = {
    predicate: predicate
  };

  triple[varKey] = this._nextVar();
  triple[lastKey] = this._lastElement;

  this._conditions.push(triple);

  this._lastElement = triple[varKey];

  return this;
}
```
- example usage
```shell
...
The Navigator API is a fluent API for LevelGraph, loosely inspired by
[Gremlin](http://markorodriguez.com/2011/06/15/graph-pattern-matching-with-gremlin-1-1/)
It allows to specify how to search our graph in a much more compact way and navigate
between vertexes.

Here is an example, using the same dataset as before:
'''javascript
db.nav("matteo").archIn("friend").archOut("friend").
  solutions(function(err, results) {
  // prints:
  // [ { x0: 'daniele', x1: 'marco' },
  //   { x0: 'daniele', x1: 'matteo' },
  //   { x0: 'lucio', x1: 'marco' },
  //   { x0: 'lucio', x1: 'matteo' } ]
  console.log(results);
...
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.as"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>as (name)](#apidoc.element.levelgraph.navigator.prototype.as)
- description and source-code
```javascript
as = function (name) {
  this._lastElement.name = name;
  return this;
}
```
- example usage
```shell
...
      // prints [ 'marco', 'matteo' ]
      console.log(results);
    });
'''

Variable names can also be specified, like so:
'''javascript
db.nav("marco").archIn("friend").as("a").archOut("friend").archOut("friend").as("a").
      solutions(function(err, friends) {

  console.log(friends); // will print [{ a: "daniele" }]
});
'''

Variables can also be bound to a specific value, like so:
...
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.bind"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>bind (value)](#apidoc.element.levelgraph.navigator.prototype.bind)
- description and source-code
```javascript
bind = function (value) {
  this._initialSolution[this._lastElement.name] = value;
  return this;
}
```
- example usage
```shell
...

  console.log(friends); // will print [{ a: "daniele" }]
});
'''

Variables can also be bound to a specific value, like so:
'''javascript
db.nav("matteo").archIn("friend").bind("lucio").archOut("friend").bind("marco").
      values(function(err, friends) {
  console.log(friends); // this will print ['marco']
});
'''

A materialized search can also be produced, like so:
'''javascript
...
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.contexts"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>contexts (query, cb)](#apidoc.element.levelgraph.navigator.prototype.contexts)
- description and source-code
```javascript
contexts = function (query, cb) {
  var args = Array.prototype.slice.call(arguments, 0)
    , callback = args.pop()
    , stream = null;

  stream = this[method].apply(this, args);

  stream.pipe(new CallbackStream({ objectMode: true }, callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.contextsStream"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>contextsStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.contextsStream)
- description and source-code
```javascript
contextsStream = function (pattern) {

  var stream = null;

  var options = {
    solution: this._initialSolution,
    materialized: pattern
  };
  stream = this.db.searchStream(this._conditions, options);

  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.go"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>go (vertex)](#apidoc.element.levelgraph.navigator.prototype.go)
- description and source-code
```javascript
go = function (vertex) {
  if (!vertex) {
    vertex = this._nextVar();
  }
  this._lastElement = vertex;
  return this;
}
```
- example usage
```shell
...

  console.log(results);
});
'''

It is also possible to change the current vertex:
'''javascript
db.nav("marco").archIn("friend").as("a").go("matteo").archOut("friend").as("b").
   solutions(function(err, solutions) {

//  solutions is: [{
//    a: "daniele",
//    b: "daniele"
//   }, {
//     a: "lucio",
...
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.solutions"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>solutions (query, cb)](#apidoc.element.levelgraph.navigator.prototype.solutions)
- description and source-code
```javascript
solutions = function (query, cb) {
  var args = Array.prototype.slice.call(arguments, 0)
    , callback = args.pop()
    , stream = null;

  stream = this[method].apply(this, args);

  stream.pipe(new CallbackStream({ objectMode: true }, callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.solutionsStream"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>solutionsStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.solutionsStream)
- description and source-code
```javascript
solutionsStream = function (pattern) {

  var stream = null;

  var options = {
    solution: this._initialSolution,
    materialized: pattern
  };
  stream = this.db.searchStream(this._conditions, options);

  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.triples"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>triples (query, cb)](#apidoc.element.levelgraph.navigator.prototype.triples)
- description and source-code
```javascript
triples = function (query, cb) {
  var args = Array.prototype.slice.call(arguments, 0)
    , callback = args.pop()
    , stream = null;

  stream = this[method].apply(this, args);

  stream.pipe(new CallbackStream({ objectMode: true }, callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.triplesStream"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>triplesStream (pattern)](#apidoc.element.levelgraph.navigator.prototype.triplesStream)
- description and source-code
```javascript
triplesStream = function (pattern) {

  var stream = null;

  var options = {
    solution: this._initialSolution,
    materialized: pattern
  };
  stream = this.db.searchStream(this._conditions, options);

  return stream;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.values"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>values (cb)](#apidoc.element.levelgraph.navigator.prototype.values)
- description and source-code
```javascript
values = function (cb) {
  var that = this
    , stream = this.valuesStream()
    , collect = function(err, results) {
        if (err) {
          cb(err);
          return;
        }

        results = results.reduce(function(acc, result) {
          if (acc.indexOf(result) < 0) {
            acc.push(result);
          }
          return acc;
        }, []);

        cb(null, results);
      };

  stream.pipe(new CallbackStream({
    objectMode: true
  }, collect));

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.navigator.prototype.valuesStream"></a>[function <span class="apidocSignatureSpan">levelgraph.navigator.prototype.</span>valuesStream ()](#apidoc.element.levelgraph.navigator.prototype.valuesStream)
- description and source-code
```javascript
valuesStream = function () {
  var stream, options;

  stream = new NavigatorStream({
    _lastElement: this._lastElement
  });

  if (this._conditions.length === 0) {
    stream.end({});
    return stream;
  }

  options = { solution: this._initialSolution };

  pump(this.db.searchStream(this._conditions, options), stream);

  return stream;
}
```
- example usage
```shell
...
  pump(this.db.searchStream(this._conditions, options), stream);

  return stream;
};

Navigator.prototype.values = function (cb) {
  var that = this
    , stream = this.valuesStream()
    , collect = function(err, results) {
if (err) {
  cb(err);
  return;
}

results = results.reduce(function(acc, result) {
...
```



# <a name="apidoc.module.levelgraph.sortjoinstream"></a>[module levelgraph.sortjoinstream](#apidoc.module.levelgraph.sortjoinstream)

#### <a name="apidoc.element.levelgraph.sortjoinstream.sortjoinstream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>sortjoinstream (options)](#apidoc.element.levelgraph.sortjoinstream.sortjoinstream)
- description and source-code
```javascript
function SortJoinStream(options) {
  if (!(this instanceof SortJoinStream)) {
    return new SortJoinStream(options);
  }

  options.objectMode = true;

  Transform.call(this, options);

  this.triple = options.triple;
  this.matcher = matcher(options.triple);
  this.db = options.db;

  var that = this;
  this.once('pipe', function(source) {
    source.on('error', function(err) {
      that.emit('error', err);
    });
  });

  this._queryMask = queryMask(options.triple);
  this._queryMask.filter = options.triple.filter;

  this.index = options.index;

  this._previousTriple = null;
  this._lastDone = null;
  this._start();
  this.limit = options.limit;
  this._limitCounter = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.super_"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.</span>super_ (options)](#apidoc.element.levelgraph.sortjoinstream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.sortjoinstream.prototype"></a>[module levelgraph.sortjoinstream.prototype](#apidoc.module.levelgraph.sortjoinstream.prototype)

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._doRead"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_doRead (triple)](#apidoc.element.levelgraph.sortjoinstream.prototype._doRead)
- description and source-code
```javascript
function doRead(triple) {

  var newsolution = this.matcher(this._lastSolution, triple)
    , key
    , otherKey
    , done = this._lastDone;

  key = genKeyWithEnding(this.index, materializer(this.triple, this._lastSolution));
  otherKey = genKey(this.index, triple);

  if (newsolution) {
    this.push(newsolution);

    if (this.limit && ++this._limitCounter === this.limit) {
      this._previousTriple = null;
      this._execLastDone();
      this._readStream.destroy();
      this._readStream = null;
      return;
    }
  }

  if (key > otherKey) {
    this._nextTriple(true);
  } else {
    this._lastDone = null;
    done();
  }
}
```
- example usage
```shell
...
}

if (!this._previousTriple && this._readStream) {
  this._previousTriple = this._readStream.read();
}

if (this._previousTriple) {
  this._doRead(this._previousTriple);
} else if (!this._readStream) {
  this.push(null);
}
};

SortJoinStream.prototype._start = function() {
var that = this;
...
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._execLastDone"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_execLastDone ()](#apidoc.element.levelgraph.sortjoinstream.prototype._execLastDone)
- description and source-code
```javascript
_execLastDone = function () {
  var that = this;
  if(that._lastDone) {
    var func = that._lastDone;
    that._lastDone = null;
    func();
  }
}
```
- example usage
```shell
...
this._readStream.on('error', function(err) {
  that.emit('error', err);
});

this._readStream.on('close', function() {
  that._readStream = null;
  if (!that._previousTriple) {
    that._execLastDone();
  }
});

this._readStream.on('readable', function() {
  if (that._lastDone) {
    that._nextTriple();
  }
...
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._flush"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_flush (cb)](#apidoc.element.levelgraph.sortjoinstream.prototype._flush)
- description and source-code
```javascript
_flush = function (cb) {
  var that = this;

  this._execLastDone();

  if (this._readStream) {
    that._readStream.destroy();
  }

  this.push(null);

  cb();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._nextTriple"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_nextTriple (skip)](#apidoc.element.levelgraph.sortjoinstream.prototype._nextTriple)
- description and source-code
```javascript
function nextTriple(skip) {
  var triple;

  if (skip) {
    this._previousTriple = null;
  }

  if (!this._previousTriple && this._readStream) {
    this._previousTriple = this._readStream.read();
  }

  if (this._previousTriple) {
    this._doRead(this._previousTriple);
  } else if (!this._readStream) {
    this.push(null);
  }
}
```
- example usage
```shell
...
  if (!that._previousTriple) {
    that._execLastDone();
  }
});

this._readStream.on('readable', function() {
  if (that._lastDone) {
    that._nextTriple();
  }
});
};

SortJoinStream.prototype._execLastDone = function() {
var that = this;
if(that._lastDone) {
...
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._start"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_start ()](#apidoc.element.levelgraph.sortjoinstream.prototype._start)
- description and source-code
```javascript
_start = function () {
  var that = this;

  this._readStream = this.db.getStream(this._queryMask, { index: this.index });

  this._readStream.on('error', function(err) {
    that.emit('error', err);
  });

  this._readStream.on('close', function() {
    that._readStream = null;
    if (!that._previousTriple) {
      that._execLastDone();
    }
  });

  this._readStream.on('readable', function() {
    if (that._lastDone) {
      that._nextTriple();
    }
  });
}
```
- example usage
```shell
...
  this._queryMask = queryMask(options.triple);
  this._queryMask.filter = options.triple.filter;

  this.index = options.index;

  this._previousTriple = null;
  this._lastDone = null;
  this._start();
  this.limit = options.limit;
  this._limitCounter = 0;
}

inherits(SortJoinStream, Transform);

SortJoinStream.prototype._nextTriple = function nextTriple(skip) {
...
```

#### <a name="apidoc.element.levelgraph.sortjoinstream.prototype._transform"></a>[function <span class="apidocSignatureSpan">levelgraph.sortjoinstream.prototype.</span>_transform (solution, encoding, done)](#apidoc.element.levelgraph.sortjoinstream.prototype._transform)
- description and source-code
```javascript
_transform = function (solution, encoding, done) {
  this._lastSolution = solution;
  this._lastDone = done;
  this._nextTriple(false);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.utilities"></a>[module levelgraph.utilities](#apidoc.module.levelgraph.utilities)

#### <a name="apidoc.element.levelgraph.utilities.createQuery"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>createQuery (pattern, options)](#apidoc.element.levelgraph.utilities.createQuery)
- description and source-code
```javascript
function createQuery(pattern, options) {
  var types = typesFromPattern(pattern)
    , preferiteIndex = options && options.index
    , index = findIndex(types, preferiteIndex)
    , key = genKey(index, pattern, '')
    , limit = pattern.limit
    , reverse = pattern.reverse || false
    , start = reverse ? applyUpperBoundChar(key) : key
    , end = reverse ? key : applyUpperBoundChar(key)
    , query = {
          start: start
        , end: end
        , reverse: reverse
        , fillCache: true
        , limit: typeof limit === 'number' && limit || -1
        , highWaterMark: 16
        , valueEncoding: 'json'
      };

  return query;
}
```
- example usage
```shell
...
'''

### Generate levelup query

Return the leveldb query for the given triple.

'''js
var query = db.createQuery({ predicate: "b"});
leveldb.createReadStream(query);
'''

## Navigator API

The Navigator API is a fluent API for LevelGraph, loosely inspired by
[Gremlin](http://markorodriguez.com/2011/06/15/graph-pattern-matching-with-gremlin-1-1/)
...
```

#### <a name="apidoc.element.levelgraph.utilities.escape"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>escape (value)](#apidoc.element.levelgraph.utilities.escape)
- description and source-code
```javascript
function escape(value) {
  if (typeof value === 'string' || value instanceof String) {
    return value.replace(/(\\|:)/g,'\\$&');
  }
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.findIndex"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>findIndex (types, preferiteIndex)](#apidoc.element.levelgraph.utilities.findIndex)
- description and source-code
```javascript
function findIndex(types, preferiteIndex) {
  var result = possibleIndexes(types)
    , index
    , there;

  there = result.some(function(r) {
    return r === preferiteIndex;
  });

  if (preferiteIndex && there) {
    index = preferiteIndex;
  } else {
    index = result[0];
  }

  return index;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.genKey"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>genKey (key, triple)](#apidoc.element.levelgraph.utilities.genKey)
- description and source-code
```javascript
function genKey(key, triple) {
  var result = key, def = defs[key], value, i;

  for (i = 0; (value = triple[def[i]]) !== null &&
              value !== undefined; i++) {
    result += '::' + escape(value);
  }

  if (i < 3) {
    result += '::';
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.genKeys"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>genKeys (triple)](#apidoc.element.levelgraph.utilities.genKeys)
- description and source-code
```javascript
function genKeys(triple) {
  var i, result = [];

  for (i = 0; i < defKeys.length; i++) {
    result.push(genKey(defKeys[i], triple));
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.generateBatch"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>generateBatch (triple, action)](#apidoc.element.levelgraph.utilities.generateBatch)
- description and source-code
```javascript
function generateBatch(triple, action) {
  if (!action) {
    action = 'put';
  }
  var json = JSON.stringify(triple);
  return genKeys(triple).map(function(key) {
    return { type: action, key: key, value: json };
  });
}
```
- example usage
```shell
...
You can also generate a 'put' and 'del' batch, so you can
manage the batching yourself:

'''javascript
var triple = { subject: "a", predicate: "b", object: "c" };

// Produces a batch of put operations
var putBatch = db.generateBatch(triple);

// Produces a batch of del operations
var delBatch = db.generateBatch(triple, 'del');
'''

### Generate levelup query
...
```

#### <a name="apidoc.element.levelgraph.utilities.maskUpdater"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>maskUpdater (pattern)](#apidoc.element.levelgraph.utilities.maskUpdater)
- description and source-code
```javascript
function maskUpdater(pattern) {
  var variables = variablesMask(pattern);
  return function(solution, mask) {
    return Object.keys(variables).reduce(function(newMask, key) {
      var variable = variables[key];
      if (variable.isBound(solution)) {
        newMask[key] = solution[variable.name];
      }
      newMask.filter = pattern.filter;
      return newMask;
    }, Object.keys(mask).reduce(function(acc, key) {
      acc[key] = mask[key];
      return acc;
    }, {}));
  };
}
```
- example usage
```shell
...

JoinStream.prototype._transform = function transform(solution, encoding, done) {
if (this._ended) {
  return done();
}

var that = this
  , newMask = this.maskUpdater(solution, this.mask);

that._lastSolution = solution;
that._readStream = this.db.getStream(newMask, this._indexPreferences);

that._readStream.on('data', that._onDataStream);
that._readStream.on('error', that._onErrorStream);
that._readStream.on('end', done);
...
```

#### <a name="apidoc.element.levelgraph.utilities.matcher"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>matcher (pattern)](#apidoc.element.levelgraph.utilities.matcher)
- description and source-code
```javascript
function matcher(pattern) {
  var variables = variablesMask(pattern);

  return function realMatcher(solution, triple) {
    var key, bindable = true, newsolution = solution;

    for (key in variables) {
      if (newsolution && variables.hasOwnProperty(key)) {
        newsolution = variables[key].bind(newsolution, triple[key]);
      }
    }

    return newsolution;
  };
}
```
- example usage
```shell
...
  this.once('pipe', function(source) {
source.on('error', function(err) {
  that.emit('error', err);
});
  });

  this._onDataStream = function onDataStream(triple) {
var newsolution = that.matcher(that._lastSolution, triple);

if (that._ended || !newsolution) {
  return;
}

that.push(newsolution);
...
```

#### <a name="apidoc.element.levelgraph.utilities.materializer"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>materializer (pattern, data)](#apidoc.element.levelgraph.utilities.materializer)
- description and source-code
```javascript
function materializer(pattern, data) {
  return Object.keys(pattern)
               .reduce(function(result, key) {

    if (pattern[key] instanceof Variable) {
      result[key] = data[pattern[key].name];
    } else {
      result[key] = pattern[key];
    }

    return result;
  }, {});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.possibleIndexes"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>possibleIndexes (types)](#apidoc.element.levelgraph.utilities.possibleIndexes)
- description and source-code
```javascript
function possibleIndexes(types) {
  var result = Object.keys(defs).filter(function(key) {
    var matches = 0;
    return defs[key].every(function (e, i) {
      if (types.indexOf(e) >= 0) {
        matches++;
        return true;
      }

      if (matches === types.length) {
        return true;
      }
    });
  });

  result.sort();

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.utilities.queryMask"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>queryMask (object)](#apidoc.element.levelgraph.utilities.queryMask)
- description and source-code
```javascript
function queryMask(object) {
  return objectMask(b, object);
}
```
- example usage
```shell
...
}

doSortQueryPlan = function(first, second) {
  if (first === null || first.stream === JoinStream) {
return null;
  }

  var firstQueryMask = utilities.queryMask(first)
, secondQueryMask = utilities.queryMask(second)
, firstVariablesMask = utilities.variablesMask(first)
, secondVariablesMask = utilities.variablesMask(second)

, firstVariables = Object.keys(firstVariablesMask).map(function(key) {
    return firstVariablesMask[key];
  })
...
```

#### <a name="apidoc.element.levelgraph.utilities.variablesMask"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>variablesMask (object)](#apidoc.element.levelgraph.utilities.variablesMask)
- description and source-code
```javascript
function variablesMask(object) {
  return objectMask(c, object);
}
```
- example usage
```shell
...
doSortQueryPlan = function(first, second) {
  if (first === null || first.stream === JoinStream) {
return null;
  }

  var firstQueryMask = utilities.queryMask(first)
, secondQueryMask = utilities.queryMask(second)
, firstVariablesMask = utilities.variablesMask(first)
, secondVariablesMask = utilities.variablesMask(second)

, firstVariables = Object.keys(firstVariablesMask).map(function(key) {
    return firstVariablesMask[key];
  })

, secondVariables = Object.keys(secondVariablesMask).map(function(key) {
...
```

#### <a name="apidoc.element.levelgraph.utilities.wrapCallback"></a>[function <span class="apidocSignatureSpan">levelgraph.utilities.</span>wrapCallback (method)](#apidoc.element.levelgraph.utilities.wrapCallback)
- description and source-code
```javascript
function wrapCallback(method) {
  return function(query, cb) {
    var args = Array.prototype.slice.call(arguments, 0)
      , callback = args.pop()
      , stream = null;

    stream = this[method].apply(this, args);

    stream.pipe(new CallbackStream({ objectMode: true }, callback));
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.variable"></a>[module levelgraph.variable](#apidoc.module.levelgraph.variable)

#### <a name="apidoc.element.levelgraph.variable.variable"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>variable (name)](#apidoc.element.levelgraph.variable.variable)
- description and source-code
```javascript
function Variable(name) {
  if (!(this instanceof Variable)) {
    return new Variable(name);
  }

  this.name = name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.variable.prototype"></a>[module levelgraph.variable.prototype](#apidoc.module.levelgraph.variable.prototype)

#### <a name="apidoc.element.levelgraph.variable.prototype.bind"></a>[function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>bind (solution, value)](#apidoc.element.levelgraph.variable.prototype.bind)
- description and source-code
```javascript
bind = function (solution, value) {
  var newsolution = {}
    , key;

  if (!this.isBindable(solution, value)) {
    return null;
  }

  for (key in solution) {
    if (solution.hasOwnProperty(key)) {
      newsolution[key] = solution[key];
    }
  }

  newsolution[this.name] = value;

  return newsolution;
}
```
- example usage
```shell
...

  console.log(friends); // will print [{ a: "daniele" }]
});
'''

Variables can also be bound to a specific value, like so:
'''javascript
db.nav("matteo").archIn("friend").bind("lucio").archOut("friend").bind("marco").
      values(function(err, friends) {
  console.log(friends); // this will print ['marco']
});
'''

A materialized search can also be produced, like so:
'''javascript
...
```

#### <a name="apidoc.element.levelgraph.variable.prototype.isBindable"></a>[function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>isBindable (solution, value)](#apidoc.element.levelgraph.variable.prototype.isBindable)
- description and source-code
```javascript
isBindable = function (solution, value) {
  return !solution[this.name] || solution[this.name] === value;
}
```
- example usage
```shell
...
this.name = name;
}

Variable.prototype.bind = function(solution, value) {
var newsolution = {}
  , key;

if (!this.isBindable(solution, value)) {
  return null;
}

for (key in solution) {
  if (solution.hasOwnProperty(key)) {
    newsolution[key] = solution[key];
  }
...
```

#### <a name="apidoc.element.levelgraph.variable.prototype.isBound"></a>[function <span class="apidocSignatureSpan">levelgraph.variable.prototype.</span>isBound (solution)](#apidoc.element.levelgraph.variable.prototype.isBound)
- description and source-code
```javascript
isBound = function (solution) {
  return solution[this.name] && true || false;
}
```
- example usage
```shell
...
var variablesMask = module.exports.variablesMask;

function maskUpdater(pattern) {
var variables = variablesMask(pattern);
return function(solution, mask) {
  return Object.keys(variables).reduce(function(newMask, key) {
    var variable = variables[key];
    if (variable.isBound(solution)) {
      newMask[key] = solution[variable.name];
    }
    newMask.filter = pattern.filter;
    return newMask;
  }, Object.keys(mask).reduce(function(acc, key) {
    acc[key] = mask[key];
    return acc;
...
```



# <a name="apidoc.module.levelgraph.writestream"></a>[module levelgraph.writestream](#apidoc.module.levelgraph.writestream)

#### <a name="apidoc.element.levelgraph.writestream.writestream"></a>[function <span class="apidocSignatureSpan">levelgraph.</span>writestream (options)](#apidoc.element.levelgraph.writestream.writestream)
- description and source-code
```javascript
function WriteStream(options) {
  if (!(this instanceof WriteStream)) {
    return new WriteStream(options);
  }

  options = options || {};
  options.objectMode = true;

  Transform.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.levelgraph.writestream.super_"></a>[function <span class="apidocSignatureSpan">levelgraph.writestream.</span>super_ (options)](#apidoc.element.levelgraph.writestream.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.levelgraph.writestream.prototype"></a>[module levelgraph.writestream.prototype](#apidoc.module.levelgraph.writestream.prototype)

#### <a name="apidoc.element.levelgraph.writestream.prototype._transform"></a>[function <span class="apidocSignatureSpan">levelgraph.writestream.prototype.</span>_transform (data, encoding, done)](#apidoc.element.levelgraph.writestream.prototype._transform)
- description and source-code
```javascript
_transform = function (data, encoding, done) {
  var that = this, i, actions = genActions(data);

  for (i = 0; i < actions.length; i++) {
    that.push(actions[i]);
  }

  done();
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
