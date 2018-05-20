# Reason React Starter

This contains my modifications to the `bsb -init` starter project from the
official docs: https://reasonml.github.io/reason-react/docs/en/installation.html

# Installation

Clone this repo into a new directory and `cd` into it:

```
$ git clone --depth=1 https://github.com/baddox/reason-react-starter.git MyApp
$ cd MyApp
```

Install all dependencies:

```
$ yarn
```

Remove the `.git` directory so that we can start over as a new repo:

```
$ rm -rf .git
```

Initialize a new repo for this directory (e.g. by following GitHub's
instructions after [creating a new repo](https://github.com/new)).

# Development

Run the following three tasks in three separate tabs (and keep them running).

* Run BuckleScript to compile ReasonML `.re` files to JavaScript (the `.js`
  files get put in `lib/js/src/` and are git ignored):

  ```
  yarn run start
  ```

* Run webpack to compile the JavaScript files into one bundle (at
  `build/app.js`):

  ```
  yarn run webpack
  ```

* Run the webpack dev server to serve up your web app locally:

  ```
  yarn run dev
  ```

# Building for production

Choose a name for your app in `bsconfig.json` and `package.json` (it should be
the same name in both).

Run `yarn run webpack:production` to generate the `index.html` and `app.js`
files in the `build/` directory.

# Todo

* Consolidate the three crazy npm tasks into just one (presumably the webpack
  dev server).
* Figure out how to require and build CSS (eject reason-scripts and see how they
  do it in their webpack config).
* Figure out Yeoman or something to allow "forking" this starter project into
  new projects without removing the `.git` directory.
