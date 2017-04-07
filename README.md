# api documentation for  [less-middleware (v2.2.0)](https://github.com/emberfeather/less.js-middleware#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-less-middleware.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-less-middleware) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-less-middleware.svg)](https://travis-ci.org/npmdoc/node-npmdoc-less-middleware)
#### LESS.js middleware for connect.

[![NPM](https://nodei.co/npm/less-middleware.png?downloads=true)](https://www.npmjs.com/package/less-middleware)

[![apidoc](https://npmdoc.github.io/node-npmdoc-less-middleware/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-less-middleware_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-less-middleware/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-less-middleware/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-less-middleware/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Randy Merrill",
        "email": "Zoramite+github@gmail.com",
        "url": "http://forthedeveloper.com"
    },
    "bugs": {
        "url": "https://github.com/emberfeather/less.js-middleware/issues"
    },
    "dependencies": {
        "less": "~2.7.1",
        "mkdirp": "~0.5.1",
        "node.extend": "~1.1.5"
    },
    "description": "LESS.js middleware for connect.",
    "devDependencies": {
        "express": "~4.14",
        "fs-extra": "~0.30",
        "mocha": "~2.5.3",
        "supertest": "~1.2"
    },
    "directories": {},
    "dist": {
        "shasum": "c3e4d512c8403685204add7bdaad7398c535c674",
        "tarball": "https://registry.npmjs.org/less-middleware/-/less-middleware-2.2.0.tgz"
    },
    "engines": {
        "node": ">= 0.7.1"
    },
    "gitHead": "7cd63270abc66b1c21ad69ef9c3ec8a6183cfc50",
    "homepage": "https://github.com/emberfeather/less.js-middleware#readme",
    "license": "MIT",
    "main": "lib/middleware.js",
    "maintainers": [
        {
            "name": "zoramite",
            "email": "Zoramite+node@gmail.com"
        },
        {
            "name": "taxilian",
            "email": "taxilian@gmail.com"
        }
    ],
    "name": "less-middleware",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/emberfeather/less.js-middleware.git"
    },
    "scripts": {
        "test": "mocha"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module less-middleware](#apidoc.module.less-middleware)
1.  object <span class="apidocSignatureSpan">less-middleware.</span>utilities

#### [module less-middleware.utilities](#apidoc.module.less-middleware.utilities)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isCompressedPath (pathname)](#apidoc.element.less-middleware.utilities.isCompressedPath)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isSourceMap ( pathname )](#apidoc.element.less-middleware.utilities.isSourceMap)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isValidPath (pathname)](#apidoc.element.less-middleware.utilities.isValidPath)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>lessError (err)](#apidoc.element.less-middleware.utilities.lessError)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>log (key, value, type)](#apidoc.element.less-middleware.utilities.log)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>logDebug (key, value, type)](#apidoc.element.less-middleware.utilities.logDebug)
1.  [function <span class="apidocSignatureSpan">less-middleware.utilities.</span>maybeCompressedSource (pathname)](#apidoc.element.less-middleware.utilities.maybeCompressedSource)



# <a name="apidoc.module.less-middleware"></a>[module less-middleware](#apidoc.module.less-middleware)



# <a name="apidoc.module.less-middleware.utilities"></a>[module less-middleware.utilities](#apidoc.module.less-middleware.utilities)

#### <a name="apidoc.element.less-middleware.utilities.isCompressedPath"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isCompressedPath (pathname)](#apidoc.element.less-middleware.utilities.isCompressedPath)
- description and source-code
```javascript
isCompressedPath = function (pathname) {
  return regex.compress.test(pathname);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.less-middleware.utilities.isSourceMap"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isSourceMap ( pathname )](#apidoc.element.less-middleware.utilities.isSourceMap)
- description and source-code
```javascript
isSourceMap = function ( pathname ){
  return regex.sourceMap.test(pathname);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.less-middleware.utilities.isValidPath"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>isValidPath (pathname)](#apidoc.element.less-middleware.utilities.isValidPath)
- description and source-code
```javascript
isValidPath = function (pathname) {
  return regex.handle.test(pathname);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.less-middleware.utilities.lessError"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>lessError (err)](#apidoc.element.less-middleware.utilities.lessError)
- description and source-code
```javascript
lessError = function (err) {
  // An error while less is processing the file.
  module.exports.log('LESS ' + err.type + ' error', err.message, 'error');
  module.exports.log('LESS File', err.filename + ' ' + err.line + ':' + err.column, 'error');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.less-middleware.utilities.log"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>log (key, value, type)](#apidoc.element.less-middleware.utilities.log)
- description and source-code
```javascript
log = function (key, value, type) {
  // Only log for errors.
  if(type !== 'error') {
    return;
  }

  console[type]("  \u001b[90m%s :\u001b[0m \u001b[36m%s\u001b[0m", key, value);
}
```
- example usage
```shell
...
  return regex.sourceMap.test(pathname);
},
isValidPath: function(pathname) {
  return regex.handle.test(pathname);
},
lessError: function(err) {
  // An error while less is processing the file.
  module.exports.log('LESS ' + err.type + ' error', err.message, 'error');
  module.exports.log('LESS File', err.filename + ' ' + err.line + ':' + err.column, 'error');
},
log: function(key, value, type) {
  // Only log for errors.
  if(type !== 'error') {
    return;
  }
...
```

#### <a name="apidoc.element.less-middleware.utilities.logDebug"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>logDebug (key, value, type)](#apidoc.element.less-middleware.utilities.logDebug)
- description and source-code
```javascript
logDebug = function (key, value, type) {
  switch(type) {
    case 'log':
    case 'info':
    case 'error':
    case 'warn':
      break;
    default:
      type = 'log';
  }

  console[type]("  \u001b[90m%s :\u001b[0m \u001b[36m%s\u001b[0m", key, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.less-middleware.utilities.maybeCompressedSource"></a>[function <span class="apidocSignatureSpan">less-middleware.utilities.</span>maybeCompressedSource (pathname)](#apidoc.element.less-middleware.utilities.maybeCompressedSource)
- description and source-code
```javascript
maybeCompressedSource = function (pathname) {
  return (regex.compress.test(pathname)
      ? pathname.replace(regex.compress, '.less')
      : pathname.replace('.css', '.less')
    );
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
