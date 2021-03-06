# npmtest-mitt

#### basic test coverage for  [mitt (v1.1.2)](https://github.com/developit/mitt)  [![npm package](https://img.shields.io/npm/v/npmtest-mitt.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-mitt) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-mitt.svg)](https://travis-ci.org/npmtest/node-npmtest-mitt)

#### Tiny 200b functional Event Emitter / pubsub.

[![NPM](https://nodei.co/npm/mitt.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mitt)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-mitt/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-mitt/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-mitt/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-mitt/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-mitt/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-mitt/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-mitt/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-mitt/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-mitt/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-mitt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-mitt/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-mitt/build/test-report.html](https://npmtest.github.io/node-npmtest-mitt/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-mitt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-mitt/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mitt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-mitt/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-mitt/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "authors": [
        "Jason Miller <jason@developit.ca>"
    ],
    "bugs": {
        "url": "https://github.com/developit/mitt/issues"
    },
    "dependencies": {},
    "description": "Tiny 200b functional Event Emitter / pubsub.",
    "devDependencies": {
        "babel-core": "^6.9.1",
        "babel-eslint": "^7.1.1",
        "babel-plugin-transform-flow-strip-types": "^6.21.0",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-stage-0": "^6.5.0",
        "babel-register": "^6.9.0",
        "chai": "^3.5.0",
        "documentation": "^4.0.0-beta4",
        "eslint": "^3.13.1",
        "flow-bin": "^0.38.0",
        "gzip-size-cli": "^1.0.0",
        "mocha": "^3.2.0",
        "npm-run-all": "^2.1.1",
        "pretty-bytes-cli": "^2.0.0",
        "rimraf": "^2.5.2",
        "rollup": "^0.41.4",
        "rollup-plugin-buble": "^0.15.0",
        "rollup-plugin-flow": "^1.1.1",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0",
        "standard-version": "^4.0.0",
        "strip-json-comments-cli": "^1.0.1",
        "uglify-js": "^2.6.2"
    },
    "directories": {},
    "dist": {
        "shasum": "380e61480d6a615b660f07abb60d51e0a4e4bed6",
        "tarball": "https://registry.npmjs.org/mitt/-/mitt-1.1.2.tgz"
    },
    "eslintConfig": {
        "parser": "babel-eslint",
        "extends": "eslint:recommended",
        "env": {
            "browser": true,
            "mocha": true,
            "es6": true
        },
        "globals": {
            "expect": true
        },
        "rules": {
            "semi": [
                2,
                "always"
            ]
        }
    },
    "files": [
        "src",
        "dist",
        "mitt.d.ts"
    ],
    "gitHead": "325d81838ee908dc0165dc1658e94c2eb4aee98a",
    "homepage": "https://github.com/developit/mitt",
    "jsnext:main": "dist/mitt.es.js",
    "keywords": [
        "events",
        "eventemitter",
        "pubsub"
    ],
    "license": "MIT",
    "main": "dist/mitt.js",
    "maintainers": [
        {
            "name": "developit"
        }
    ],
    "module": "dist/mitt.es.js",
    "name": "mitt",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/developit/mitt.git"
    },
    "scripts": {
        "build": "npm-run-all --silent clean -p rollup -p minify:* -s docs size",
        "bump": "standard-version",
        "clean": "rimraf dist",
        "docs": "documentation readme src/index.js --section API -q",
        "lint": "eslint src test",
        "minify:cjs": "uglifyjs $npm_package_main -cm toplevel -o $npm_package_main -p relative --in-source-map ${npm_package_main}.map --source-map ${npm_package_main}.map",
        "minify:umd": "uglifyjs $npm_package_umd_main -cm -o $npm_package_umd_main -p relative --in-source-map ${npm_package_umd_main}.map --source-map ${npm_package_umd_main}.map",
        "release": "npm run build -s && npm run bump && git push --follow-tags origin master && npm publish",
        "rollup": "rollup -c",
        "size": "echo \"Gzipped Size: $(strip-json-comments --no-whitespace $npm_package_main | gzip-size | pretty-bytes)\"",
        "test": "flow && npm run lint && npm run testonly",
        "testonly": "mocha --compilers js:babel-register test/**/*.js"
    },
    "typings": "./mitt.d.ts",
    "umd:main": "dist/mitt.umd.js",
    "version": "1.1.2",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
