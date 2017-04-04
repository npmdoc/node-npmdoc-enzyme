# api documentation for  [enzyme (v2.8.0)](https://github.com/airbnb/enzyme#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-enzyme.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-enzyme) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-enzyme.svg)](https://travis-ci.org/npmdoc/node-npmdoc-enzyme)
#### JavaScript Testing utilities for React

[![NPM](https://nodei.co/npm/enzyme.png?downloads=true)](https://www.npmjs.com/package/enzyme)

[![apidoc](https://npmdoc.github.io/node-npmdoc-enzyme/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-enzyme_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-enzyme/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-enzyme/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-enzyme/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Leland Richardson",
        "email": "leland.richardson@airbnb.com"
    },
    "bugs": {
        "url": "https://github.com/airbnb/enzyme/issues"
    },
    "dependencies": {
        "cheerio": "^0.22.0",
        "function.prototype.name": "^1.0.0",
        "is-subset": "^0.1.1",
        "lodash": "^4.17.2",
        "object-is": "^1.0.1",
        "object.assign": "^4.0.4",
        "object.entries": "^1.0.3",
        "object.values": "^1.0.3",
        "uuid": "^2.0.3"
    },
    "description": "JavaScript Testing utilities for React",
    "devDependencies": {
        "babel-cli": "^6.18.0",
        "babel-core": "^6.18.2",
        "babel-eslint": "^7.1.0",
        "babel-loader": "^6.2.7",
        "babel-preset-airbnb": "^2.1.1",
        "babel-register": "^6.18.0",
        "chai": "^3.5.0",
        "coveralls": "^2.11.15",
        "enzyme-example-jest": "^0.1.0",
        "enzyme-example-karma": "^0.1.1",
        "enzyme-example-karma-webpack": "^0.1.4",
        "enzyme-example-mocha": "^0.1.0",
        "enzyme-example-react-native": "^0.1.0",
        "eslint": "^3.10.2",
        "eslint-config-airbnb": "^13.0.0",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-jsx-a11y": "^2.2.3",
        "eslint-plugin-react": "^6.7.1",
        "gitbook-cli": "^1.0.1",
        "in-publish": "^2.0.0",
        "istanbul": "^1.0.0-alpha.2",
        "jsdom": "^6.1.0",
        "json-loader": "^0.5.4",
        "karma": "^1.3.0",
        "karma-chrome-launcher": "^1.0.1",
        "karma-firefox-launcher": "^1.0.0",
        "karma-mocha": "^1.2.0",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-webpack": "^1.8.0",
        "mocha": "^3.1.2",
        "rimraf": "^2.5.4",
        "safe-publish-latest": "^1.1.1",
        "sinon": "^1.17.6",
        "webpack": "^1.13.3"
    },
    "directories": {},
    "dist": {
        "shasum": "86cc1fc96e5cbd7695766dd6e89deb13a0aead51",
        "tarball": "https://registry.npmjs.org/enzyme/-/enzyme-2.8.0.tgz"
    },
    "gitHead": "a4c63a19f8648942b3fca72bf34d863cfa0c6dd9",
    "homepage": "https://github.com/airbnb/enzyme#readme",
    "keywords": [
        "javascript",
        "shallow rendering",
        "shallowRender",
        "test",
        "reactjs",
        "react",
        "flux",
        "testing",
        "test utils",
        "assertion helpers",
        "tdd",
        "mocha"
    ],
    "license": "MIT",
    "main": "build",
    "maintainers": [
        {
            "name": "airbnb",
            "email": "jordan.harband+npm@airbnb.com"
        },
        {
            "name": "gdborton",
            "email": "gdborton@gmail.com"
        },
        {
            "name": "intelligibabble",
            "email": "leland.m.richardson@gmail.com"
        },
        {
            "name": "ljharb",
            "email": "ljharb@gmail.com"
        }
    ],
    "name": "enzyme",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "0.13.x || 0.14.x || ^15.0.0-0 || 15.x"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/airbnb/enzyme.git"
    },
    "scripts": {
        "build": "babel src --out-dir build",
        "check": "npm run lint && npm run test:all",
        "clean": "rimraf build",
        "docs:build": "npm run docs:prepare && gitbook build",
        "docs:clean": "rimraf _book",
        "docs:prepare": "gitbook install",
        "docs:publish": "npm run docs:clean && npm run docs:build && cd _book && git init && git commit --allow-empty -m 'update book' && git fetch git@github.com:airbnb/enzyme.git gh-pages && git checkout -b gh-pages && git add . && git commit -am 'update book' && git push git@github.com:airbnb/enzyme.git gh-pages --force",
        "docs:watch": "npm run docs:prepare && gitbook serve",
        "lint": "eslint --ext js,jsx src test",
        "postversion": "git push && git push --tags && npm run clean && npm run docs:publish",
        "prepublish": "not-in-publish || (npm run clean && npm run build && safe-publish-latest)",
        "pretest": "npm run lint",
        "preversion": "npm run clean && npm run check",
        "react:13": "rimraf node_modules/.bin/npm && npm run react:clean && npm i react@0.13 && npm install",
        "react:14": "rimraf node_modules/.bin/npm && npm run react:clean && npm i react@0.14 react-dom@0.14 react-addons-test-utils@0.14 && npm install",
        "react:15": "rimraf node_modules/.bin/npm && npm run react:clean && npm i react@15 react-dom@15 react-addons-test-utils@15 && npm install",
        "react:clean": "rimraf node_modules/react node_modules/react-dom node_modules/react-addons-test-utils",
        "test": "npm run clean && npm run build && npm run test:only",
        "test:all": "npm run react:13 && npm run test:only && npm run react:14 && npm run test:only && npm run react:15 && npm run test:only",
        "test:env": "sh ./example-test.sh",
        "test:karma": "karma start",
        "test:only": "mocha --recursive test",
        "test:single": "mocha --watch",
        "test:watch": "mocha --recursive --watch test",
        "travis": "babel-node ./node_modules/.bin/istanbul cover --report html _mocha -- test --recursive",
        "version": "npm run build"
    },
    "version": "2.8.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module enzyme](#apidoc.module.enzyme)
1.  [function <span class="apidocSignatureSpan">enzyme.</span>ReactWrapper (nodes, root)](#apidoc.element.enzyme.ReactWrapper)
1.  [function <span class="apidocSignatureSpan">enzyme.</span>ShallowWrapper (nodes, root)](#apidoc.element.enzyme.ShallowWrapper)
1.  [function <span class="apidocSignatureSpan">enzyme.</span>mount (node, options)](#apidoc.element.enzyme.mount)
1.  [function <span class="apidocSignatureSpan">enzyme.</span>render (node)](#apidoc.element.enzyme.render)
1.  [function <span class="apidocSignatureSpan">enzyme.</span>shallow (node, options)](#apidoc.element.enzyme.shallow)



# <a name="apidoc.module.enzyme"></a>[module enzyme](#apidoc.module.enzyme)

#### <a name="apidoc.element.enzyme.ReactWrapper"></a>[function <span class="apidocSignatureSpan">enzyme.</span>ReactWrapper (nodes, root)](#apidoc.element.enzyme.ReactWrapper)
- description and source-code
```javascript
function ReactWrapper(nodes, root) {
  var options = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : {};

  _classCallCheck(this, ReactWrapper);

  if (!global.window && !global.document) {
    throw new Error('It looks like you called 'mount()' without a global document being loaded.');
  }

  if (!root) {
    var ReactWrapperComponent = (0, _ReactWrapperComponent2['default'])(nodes, options);
    this.component = (0, _reactCompat.renderWithOptions)(_react2['default'].createElement(ReactWrapperComponent, {
      Component: nodes.type,
      props: nodes.props,
      context: options.context
    }), options);
    this.root = this;
    this.node = this.component.getWrappedComponent();
    this.nodes = [this.node];
    this.length = 1;
  } else {
    this.component = null;
    this.root = root;
    if (!nodes) {
      this.nodes = [];
    } else if (!Array.isArray(nodes)) {
      this.node = nodes;
      this.nodes = [nodes];
    } else {
      this.node = nodes[0];
      this.nodes = nodes;
    }
    this.length = this.nodes.length;
  }
  this.options = options;
  this.complexSelector = new _ComplexSelector2['default'](_MountedTraversal.buildInstPredicate, findWhereUnwrapped, _MountedTraversal
.childrenOfInst);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.enzyme.ShallowWrapper"></a>[function <span class="apidocSignatureSpan">enzyme.</span>ShallowWrapper (nodes, root)](#apidoc.element.enzyme.ShallowWrapper)
- description and source-code
```javascript
function ShallowWrapper(nodes, root) {
  var _this = this;

  var options = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : {};

  _classCallCheck(this, ShallowWrapper);

  validateOptions(options);
  if (!root) {
    this.root = this;
    this.unrendered = nodes;
    this.renderer = (0, _reactCompat.createShallowRenderer)();
    (0, _Utils.withSetStateAllowed)(function () {
      (0, _reactCompat.batchedUpdates)(function () {
        _this.renderer.render(nodes, options.context);
        var instance = _this.instance();
        if (options.lifecycleExperimental && instance && typeof instance.componentDidMount === 'function') {
          instance.componentDidMount();
        }
      });
    });
    this.node = this.renderer.getRenderOutput();
    this.nodes = [this.node];
    this.length = 1;
  } else {
    this.root = root;
    this.unrendered = null;
    this.renderer = null;
    if (!Array.isArray(nodes)) {
      this.node = nodes;
      this.nodes = [nodes];
    } else {
      this.node = nodes[0];
      this.nodes = nodes;
    }
    this.length = this.nodes.length;
  }
  this.options = options;
  this.complexSelector = new _ComplexSelector2['default'](_ShallowTraversal.buildPredicate, findWhereUnwrapped, _ShallowTraversal
.childrenOfNode);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.enzyme.mount"></a>[function <span class="apidocSignatureSpan">enzyme.</span>mount (node, options)](#apidoc.element.enzyme.mount)
- description and source-code
```javascript
function mount(node, options) {
  return new _ReactWrapper2['default'](node, null, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.enzyme.render"></a>[function <span class="apidocSignatureSpan">enzyme.</span>render (node)](#apidoc.element.enzyme.render)
- description and source-code
```javascript
function render(node) {
  var options = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : {};

  if (options.context && (node.type.contextTypes || options.childContextTypes)) {
    var childContextTypes = (0, _object2['default'])({}, node.type.contextTypes || {}, options.childContextTypes);
    var ContextWrapper = createContextWrapperForNode(node, options.context, childContextTypes);
    var _html = (0, _reactCompat.renderToStaticMarkup)(_react2['default'].createElement(ContextWrapper, null));
    return _cheerio2['default'].load(_html).root();
  }
  var html = (0, _reactCompat.renderToStaticMarkup)(node);
  return _cheerio2['default'].load(html).root();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.enzyme.shallow"></a>[function <span class="apidocSignatureSpan">enzyme.</span>shallow (node, options)](#apidoc.element.enzyme.shallow)
- description and source-code
```javascript
function shallow(node, options) {
  return new _ShallowWrapper2['default'](node, null, options);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
