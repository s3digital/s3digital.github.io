# Introduction
This theme is Jekyll theme which is supported by github pages out-of-the-box. 

The theme uses gulp to manage js dependencies.

Please familiarise with github pages https://pages.github.com/

# How it works
There are 2 branches in this repo which are important. 
- `develop` which contains the full site code
- `master` which is the generated code

github.io renders/processes `master` branch from <username>.github.io repository and makes it available at https://<username>.github.io. This minimises our infrastructure to get started. 

Github pages can process jekyll theme which makes it easier to work with website. 

Most of the configurations are available in `_config.yml` file. Please go through it first to find if you need to change text in the site.

You might have to tinker with other html files as needed.


*** Developers should only make changes to develop ***


# For local setup do,
```
bundle update
npm install

```

To deploy to master branch
```
gulp deploy
```

=================================================
=====     jekyll-gulp-sass-browser-sync     =====
=================================================
```
A project including full setup for Jekyll, GulpJS, SASS, AutoPrefixer &amp; BrowserSync

## System Preparation

To use this project, you'll need the following things installed on your machine.

1. [Jekyll](http://jekyllrb.com/) - `$ gem install jekyll`
2. [Jekyll-Archives](http://jekyllrb.com) - `$ bundle install`
3. [NodeJS](http://nodejs.org) - use the installer.
4. [GulpJS](https://github.com/gulpjs/gulp) - `$ npm install -g gulp` (mac users may need sudo)

## Local Installation

1. Inside the directory, run `npm install`.
2. Enjoy

## Usage

**development mode**

This will give you file watching, browser synchronisation, auto-rebuild, CSS injecting etc etc.

```shell
$ gulp
```

**jekyll**

As this is just a Jekyll project, you can use any of the commands listed in their [docs](http://jekyllrb.com/docs/usage/)

## Deploy with Gulp

You can easily deploy your site build to a gh-pages branch. First, follow the instructions at [gulp-gh-pages](https://github.com/rowoot/gulp-gh-pages) to get your branch prepared for the deployment and to install the module. Then, in `gulpfile.js` you'll want to include something like the code below. `gulp.src()` needs to be the path to your final site folder, which by default will be `_site`. If you change the `destination` in your `_config.yml` file, be sure to reflect that in your gulpfile.



```javascript
var deploy = require("gulp-gh-pages");

gulp.task("deploy", ["jekyll-build"], function () {
    return gulp.src("./_site/**/*")
        .pipe(deploy());
});
```
