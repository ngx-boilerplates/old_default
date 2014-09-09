# Harp boilerplate for an AngularJS app

Start writing code, stop worrying about the server!

**Zero configuration required!**

This boilerplate combines all best practices of:

- the official [Google recommended AngularJS application structure](https://docs.google.com/document/d/1XXMvReO8-Awi1EZXAXS4PzDzdNvV6pGcuaF4Q9821Es/pub)
- the fantastic [AngularJS styleguide](https://github.com/toddmotto/angularjs-styleguide) by [Todd Motto](http://toddmotto.com/)
- the lovely [HarpJS](http://harpjs.com) web server


Component based approach:

- add/remove features by adding/removing components
- add/remove components by adding/removing files
- each components has its own styles, scripts and templates

What it does:

- creates an entire directory structure for your AngularJS application
- creates the initial AngularJS components so you can immediately start working on your own code
- allows you to change all the generated boilerplate to your liking

Special features:

- use your favorite template language: Jade, EJS, Markdown, vanilla HTML or use them all together
- use the most suited template language some specific content block and include it as a partial in another language e.g. include `partial.md` inside `index.jade` and it will automatically render fine
- supports a `development` and a `production` environment
- uses Harp as built-in web server to develop locally or run in production
- supports compilation to a static website to host on any web server

## Installation

First make sure you have Harp and Bower installed:

```sh
$ sudo npm install -g harp
$ sudo npm install -g bower
```

Then initialize the boilerplate:

```sh
$ harp init -b jvandemo/hb-angular myproject
```

Change the directory to the new `myproject` directory:

```sh
$ cd myproject
```

Use bower to install the latest dependencies:

```sh
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