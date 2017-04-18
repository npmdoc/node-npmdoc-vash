# npmdoc-vash

#### api documentation for  [vash (v0.12.2)](https://github.com/kirbysayshi/vash)  [![npm package](https://img.shields.io/npm/v/npmdoc-vash.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-vash) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-vash.svg)](https://travis-ci.org/npmdoc/node-npmdoc-vash)

#### Razor syntax for JS templating

[![NPM](https://nodei.co/npm/vash.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/vash)

- [https://npmdoc.github.io/node-npmdoc-vash/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-vash/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-vash/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-vash/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-vash/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-vash/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andrew Petersen"
    },
    "bin": {
        "vash": "./bin/vash"
    },
    "bugs": {
        "url": "https://github.com/kirbysayshi/vash/issues"
    },
    "contributors": [
        {
            "name": "Andrew Petersen",
            "url": "http://kirbysayshi.com"
        },
        {
            "name": "Roy Haddad"
        },
        {
            "name": "Ron Otten"
        }
    ],
    "dependencies": {
        "commander": "~1.1.1",
        "debug": "^2.2.0",
        "uglify-js": "^2.6.2"
    },
    "description": "Razor syntax for JS templating",
    "devDependencies": {
        "browserify": "^13.0.0",
        "coverify": "^1.4.1",
        "envify": "^3.4.0",
        "jshint": "0.8.0",
        "marked": "~0.2.8",
        "semver": "~1",
        "vows": "^0.8.1"
    },
    "directories": {},
    "dist": {
        "shasum": "47c22f60e21ce9d9452123e124cbd60dbafaba80",
        "tarball": "https://registry.npmjs.org/vash/-/vash-0.12.2.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "gitHead": "ae722ebb7a232d18029a41c39a89eec125ef3239",
    "homepage": "https://github.com/kirbysayshi/vash",
    "keywords": [
        "razor",
        "parser",
        "template",
        "express"
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "kirbysayshi"
        }
    ],
    "name": "vash",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/kirbysayshi/vash.git"
    },
    "scripts": {
        "build": "browserify index.js --standalone vash > build/vash.js && browserify --standalone vash runtime.js > build/vash-runtime.js && browserify --standalone vash --external fs --external path lib/helpers/index.js > build/vash-runtime-all.js",
        "coverage": "VASHPATH=../../index.js VASHRUNTIMEPATH=../../runtime.js browserify -t envify -t coverify test/vows/vash.test.js | node | coverify",
        "docs": "scripts/docs.sh",
        "docs-dev": "scripts/docs-dev.sh",
        "prepublish": "npm run test && npm run build",
        "test": "VASHPATH=../../index.js VASHRUNTIMEPATH=../../runtime.js vows test/vows/vash.*.js --spec"
    },
    "version": "0.12.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
