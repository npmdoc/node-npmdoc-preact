# npmdoc-preact

#### basic api documentation for  [preact (v8.1.0)](https://github.com/developit/preact)  [![npm package](https://img.shields.io/npm/v/npmdoc-preact.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-preact) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-preact.svg)](https://travis-ci.org/npmdoc/node-npmdoc-preact)

#### Fast 3kb React alternative with the same ES6 API. Components & Virtual DOM.

[![NPM](https://nodei.co/npm/preact.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/preact)

- [https://npmdoc.github.io/node-npmdoc-preact/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-preact/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-preact/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-preact/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-preact/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-preact/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jason Miller"
    },
    "bugs": {
        "url": "https://github.com/developit/preact/issues"
    },
    "dependencies": {},
    "description": "Fast 3kb React alternative with the same ES6 API. Components & Virtual DOM.",
    "dev:main": "dist/preact.dev.js",
    "devDependencies": {
        "babel": "^5.8.23",
        "babel-core": "^5.8.24",
        "babel-eslint": "^6.1.0",
        "babel-loader": "^5.3.2",
        "babel-runtime": "^5.8.24",
        "chai": "^3.4.1",
        "copyfiles": "^1.0.0",
        "core-js": "^2.4.1",
        "coveralls": "^2.11.15",
        "cross-env": "^3.1.3",
        "diff": "^3.0.0",
        "eslint": "^3.0.0",
        "eslint-plugin-react": "^6.0.0",
        "gzip-size-cli": "^1.0.0",
        "isparta-loader": "^2.0.0",
        "jscodeshift": "^0.3.25",
        "karma": "^1.1.0",
        "karma-babel-preprocessor": "^5.2.2",
        "karma-chai": "^0.1.0",
        "karma-chai-sinon": "^0.1.5",
        "karma-chrome-launcher": "^2.0.0",
        "karma-coverage": "^1.0.0",
        "karma-mocha": "^1.1.1",
        "karma-mocha-reporter": "^2.0.4",
        "karma-phantomjs-launcher": "^1.0.1",
        "karma-sauce-launcher": "^1.1.0",
        "karma-source-map-support": "^1.1.0",
        "karma-sourcemap-loader": "^0.3.6",
        "karma-webpack": "^2.0.1",
        "mocha": "^3.0.1",
        "npm-run-all": "^4.0.0",
        "phantomjs-prebuilt": "^2.1.7",
        "rimraf": "^2.5.3",
        "rollup": "^0.40.0",
        "rollup-plugin-babel": "^1.0.0",
        "rollup-plugin-memory": "^2.0.0",
        "rollup-plugin-node-resolve": "^2.0.0",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0",
        "typescript": "^2.2.2",
        "uglify-js": "^2.7.5",
        "webpack": "^1.13.1"
    },
    "directories": {},
    "dist": {
        "shasum": "f035b808eebb74e46d56246b02ca0f190b6d6574",
        "tarball": "https://registry.npmjs.org/preact/-/preact-8.1.0.tgz"
    },
    "eslintConfig": {
        "extends": "./config/eslint-config.js"
    },
    "files": [
        "devtools",
        "src",
        "dist",
        "devtools.js",
        "devtools.js.map",
        "typings.json"
    ],
    "gitHead": "ca2d9217a7d60f0ae17d8be07297e301d4638e3f",
    "greenkeeper": {
        "ignore": [
            "rollup-plugin-babel",
            "babel",
            "babel-core",
            "babel-eslint",
            "babel-loader",
            "babel-runtime",
            "jscodeshift"
        ]
    },
    "homepage": "https://github.com/developit/preact",
    "jsnext:main": "src/preact.js",
    "keywords": [
        "preact",
        "react",
        "virtual dom",
        "vdom",
        "components",
        "virtual",
        "dom"
    ],
    "license": "MIT",
    "main": "dist/preact.js",
    "maintainers": [
        {
            "name": "developit"
        }
    ],
    "minified:main": "dist/preact.min.js",
    "name": "preact",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/developit/preact.git"
    },
    "scripts": {
        "build": "npm-run-all --silent clean transpile copy-flow-definition copy-typescript-definition strip optimize minify size",
        "clean": "rimraf dist/ devtools.js devtools.js.map",
        "copy-flow-definition": "copyfiles -f src/preact.js.flow dist",
        "copy-typescript-definition": "copyfiles -f src/preact.d.ts dist",
        "lint": "eslint devtools src test",
        "minify": "uglifyjs dist/preact.js -c collapse_vars,evaluate,screw_ie8,unsafe,loops=false,keep_fargs=false,pure_getters,unused,dead_code -m -o dist/preact.min.js -p relative --in-source-map dist/preact.js.map --source-map dist/preact.min.js.map",
        "optimize": "uglifyjs dist/preact.dev.js -c conditionals=false,sequences=false,loops=false,join_vars=false,collapse_vars=false --pure-funcs=Object.defineProperty --mangle-props --mangle-regex=\"/^(_|normalizedNodeName|nextBase|prev[CPS]|_parentC)/\" --name-cache config/properties.json -b width=120,quote_style=3 -o dist/preact.js -p relative --in-source-map dist/preact.dev.js.map --source-map dist/preact.js.map",
        "prepublish": "npm run build",
        "release": "cross-env npm run smart-release",
        "size": "node -e \"process.stdout.write('gzip size: ')\" && gzip-size dist/preact.min.js",
        "smart-release": "npm run build && npm test && git commit -am $npm_package_version && git tag $npm_package_version && git push && git push --tags && npm publish",
        "strip": "jscodeshift --run-in-band -s -t config/codemod-strip-tdz.js dist/preact.dev.js && jscodeshift --run-in-band -s -t config/codemod-const.js dist/preact.dev.js",
        "test": "npm-run-all lint --parallel test:mocha test:karma test:ts",
        "test:karma": "karma start test/karma.conf.js --single-run",
        "test:karma:watch": "npm run test:karma -- no-single-run",
        "test:mocha": "mocha --recursive --compilers js:babel/register test/shared test/node",
        "test:mocha:watch": "npm run test:mocha -- --watch",
        "test:ts": "tsc -p test/ts/",
        "transpile": "npm-run-all transpile:main transpile:devtools",
        "transpile:devtools": "rollup -c config/rollup.config.devtools.js -o devtools.js -m devtools.js.map",
        "transpile:main": "rollup -c config/rollup.config.js -m dist/preact.dev.js.map -n preact -o dist/preact.dev.js"
    },
    "typings": "./dist/preact.d.ts",
    "version": "8.1.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
