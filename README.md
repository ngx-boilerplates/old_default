# Harp boilerplate for an AngularJS app

Harp + AngularJS = absolute awesomeness!

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

## Unit tests

To run unit tests:

```sh
$ gulp test
```

This will run all tests in `public/**/_build/**/*.spec.js`.

## Gulp

Gulp is used to:

- selectively copy specific files from the Bower components to the `public/vendor` directory
- build individual components from all `_build` directories into the `public/build` directory
 
## Changelog

### v0.1.0

- Initial boilerplate