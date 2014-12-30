# Littlstar Developer Portal

This is the official Littlstar Developer Portal.

## Clone/Initialize

This portal is built on top of Jekyll, so a current version of Ruby and the Bundler gem are required.

```bash
git clone git@github.com:littlstar/littlstar.github.io.git
```

The site can be compiled and served locally by running:

```bash
jekyll s
```

## Configuration

Global site configuration is stored in the `_config.yml` file.

## Assets

### SASS/SCSS

All sass and scss assets are stored in the `_sass` directory. This is a Jekyll default path. The one exception is the littlstar.scss "manifest" file. This file lives in the `css` directory. The basic structure of these files is as follows:

1. `littlstar.scss` is responsible for loading all other style assets as well as for defining and overriding the Foundation defaults.
2. `_functions.scss` is the Foundation utility function declaration file.
3. `_foundation.scss` is the Foundation manifest file, responsible for `@import`ing the necessary components from the `foundation` directory.
4. `_font-awesome.scss` is the Font Awesome manifest file, responsible for `@import`ing the necessary components from the `font-awesome` directory.
5. `_highlighting.scss` is created by Jekyll when a new site is first generated. It is responsible for syntax highlighting of code samples.

All sass/scss assets are compiled by Jekyll into a single css file when the site is built or rebuilt.

### JS

There are no Javascript assets in this project. They are all loaded off of CDNs either in `_includes/head.html` or `_layouts/default.html`.

