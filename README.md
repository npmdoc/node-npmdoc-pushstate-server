# api documentation for  [pushstate-server (v3.0.0)](https://github.com/scottcorgan/pushstate-server#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-pushstate-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pushstate-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pushstate-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pushstate-server)
#### Static file server that works with HTML5 Pushstate.

[![NPM](https://nodei.co/npm/pushstate-server.png?downloads=true)](https://www.npmjs.com/package/pushstate-server)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pushstate-server_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Scott Corgan"
    },
    "bin": {
        "pushstate-server": "./bin/pushstate-server"
    },
    "bugs": {
        "url": "https://github.com/scottcorgan/pushstate-server/issues"
    },
    "dependencies": {
        "compression": "1.6.2",
        "connect": "3.6.0",
        "connect-static-file": "1.1.2",
        "serve-static": "1.12.0"
    },
    "description": "Static file server that works with HTML5 Pushstate.",
    "devDependencies": {
        "@tap-format/spec": "0.2.0",
        "got": "6.7.1",
        "prettier": "0.20.0",
        "tape": "4.6.3"
    },
    "directories": {},
    "dist": {
        "shasum": "85608b6fc76fb2e058584596151d6e6f4b250914",
        "tarball": "https://registry.npmjs.org/pushstate-server/-/pushstate-server-3.0.0.tgz"
    },
    "gitHead": "1fbfdb2d201d860b6248cadbf4801f86805e12b4",
    "homepage": "https://github.com/scottcorgan/pushstate-server#readme",
    "keywords": [
        "pushstate",
        "html5",
        "static",
        "server"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "scottcorgan",
            "email": "scottcorgan@gmail.com"
        }
    ],
    "name": "pushstate-server",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/scottcorgan/pushstate-server.git"
    },
    "scripts": {
        "format": "prettier --write \"index.js\" \"test/index.js\"",
        "test": "npm run format && npm run test-runner",
        "test-runner": "tape test/index.js | tap-format-spec"
    },
    "version": "3.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pushstate-server](#apidoc.module.pushstate-server)
1.  [function <span class="apidocSignatureSpan">pushstate-server.</span>start (options, _onStarted)](#apidoc.element.pushstate-server.start)



# <a name="apidoc.module.pushstate-server"></a>[module pushstate-server](#apidoc.module.pushstate-server)

#### <a name="apidoc.element.pushstate-server.start"></a>[function <span class="apidocSignatureSpan">pushstate-server.</span>start (options, _onStarted)](#apidoc.element.pushstate-server.start)
- description and source-code
```javascript
start = function (options, _onStarted) {
  options = options || {};

  let port = options.port || process.env.PORT || PORT;
  let directory = options.directory || DIRECTORY;
  let directories = options.directories || [directory];
  let file = options.file || FILE;
  let host = options.host || HOST;
  let onStarted = _onStarted || function() {};

  app.use(compression());

  // First, check the file system
  directories.forEach(directory =>
    app.use(serveStatic(directory, { extensions: ["html"] })));

  // Then, serve the fallback file
  app.use(serveStaticFile(path.join(directory, file)));

  const server = app.listen(port, host, err =>
    onStarted(err, server.address()));

  return server;
}
```
- example usage
```shell
...
'''

## Usage

'''js
var server = require('pushstate-server');

server.start({
  port: 3000,
  directory: './public'
});
'''

or for multiple directories
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
