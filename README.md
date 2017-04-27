# npmdoc-pushstate-server

#### basic api documentation for  [pushstate-server (v3.0.0)](https://github.com/scottcorgan/pushstate-server#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-pushstate-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pushstate-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pushstate-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pushstate-server)

#### Static file server that works with HTML5 Pushstate.

[![NPM](https://nodei.co/npm/pushstate-server.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/pushstate-server)

- [https://npmdoc.github.io/node-npmdoc-pushstate-server/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pushstate-server/build/apidoc.html)

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
            "name": "scottcorgan"
        }
    ],
    "name": "pushstate-server",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
