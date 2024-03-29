![AngularJS Express](http://i.imgur.com/nTj9QgN.png)

## Default boilerplate for AngularJS Express

**Zero configuration required!**

This boilerplate combines all best practices of:

- the official [Google recommended AngularJS application structure](https://docs.google.com/document/d/1XXMvReO8-Awi1EZXAXS4PzDzdNvV6pGcuaF4Q9821Es/pub)
- the fantastic [AngularJS styleguide](https://github.com/toddmotto/angularjs-styleguide) by [Todd Motto](http://toddmotto.com/)
- the lovely [HarpJS](http://harpjs.com) web server

Component based approach:

- add/remove features by adding/removing components
- add/remove components by adding/removing files
- each components has its own styles, scripts and templates

## Installation

First make sure you have AngularJS Express installed:

```sh
$ sudo npm install -g ngx-cli
```

Then initialize the boilerplate:

```sh
$ ngx init myproject
```

Change the directory to the new `myproject` directory:

```sh
$ cd myproject
```

Install the latest dependencies:

```sh
$ npm install
$ bower install
```

Run gulp to assemble the concatenated AngularJS library:

```sh
$ gulp
```

Start the harp server from your project directory:

```sh
$ harp server
```

And navigate to `http://localhost:9000` in your browser:

![Homepage](http://i.imgur.com/dORKysf.png)

## How it works

All action happens in the `public` directory, so let's have a look at its structure:

```sh
public
├── 200.jade
├── _build                          # main _build directory for global app stuff
│   ├── app.config.module.js        # Example 'app.config' module
│   ├── app.config.module.spec.js   # Put your unit tests here too, Karma will find them for you
│   ├── app.config.router.js        # Configure the router
│   ├── app.less                    # Global app styles that you want Gulp to add to /public/build/css/app.css
│   ├── app.module.js               # Main 'app' module
│   └── app.module.spec.js          # Sample unit tests for main 'app' module
├── build                           # Build directory where files built by Gulp are saved
│   ├── css
│   │   ├── app.css                 # All .less files from _build directories are concatenated here
│   │   └── app.min.css             # Minified version for production
│   └── js
│       ├── app.js                  # All .js files from _build directories are concatenated here
│       └── app.min.js              # Minified version for production
└── components
    ├── footer                      # Example footer component
    │   ├── _build                  # Component _build directory with files that you want Gulp to build
    │   │   └── footer.less         # Styles that you want to add to /public/build/css/app.css
    │   └── footer.jade             # Jade file will be compiled to HTML automatically
    ├── header                      # Example header component
    │   ├── _build                  # Component _build directory with files that you want Gulp to build
    │   │   └── header.less         # Styles that you want to add to /public/build/css/app.css
    │   └── header.jade             # Jade file will be compiled to HTML automatically
    └── homepage                    # Example homepage component
        ├── _build                  # Component _build directory with files that you want Gulp to build
        │   └── homepage.routes.js  # JavaScript code that you want to add to /public/build/js/app.js
        └── homepage.jade           # Jade file will be compiled to HTML automatically
```

## Unit tests

To run unit tests:

```sh
$ gulp test
```

This will run all tests in `public/**/_build/**/*.spec.js`.

## Generate documentation

To generate documentation:

```sh
$ gulp docs
```

## Gulp

Gulp is used to:

- selectively copy specific files from the Bower components to the `public/vendor` directory
- build individual components from all `_build` directories into the `public/build` directory
 
## Changelog

### v0.1.0

- Initial boilerplate