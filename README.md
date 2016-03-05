[![Build Status](https://travis-ci.org/lambdacreatives/tofino.svg)](https://travis-ci.org/lambdacreatives/tofino) [![devDependency Status](https://david-dm.org/lambdacreatives/tofino/dev-status.svg)](https://david-dm.org/lambdacreatives/tofino#info=devDependencies) [![Deployment status from DeployBot](https://lambdacreatives.deploybot.com/badge/77558060036000/47551.svg)](http://deploybot.com)

![Tofino](https://raw.githubusercontent.com/mrchimp/tofino/master/screenshot.png)

# Tofino

A WordPress starter theme for jumpstarting custom theme development.

Developed by [Daniel Hewes](https://github.com/danimalweb), [Jake Gully](https://github.com/mrchimp).

[Demo](http://tofino.lambdacreatives.com)

## Requirements

| Prerequisite              | How to check  | How to install                                  |
| ------------------------- | ------------- | ----------------------------------------------- |
| PHP >= 5.4.x              | `php -v`      | [php.net](http://php.net/manual/en/install.php) |
| Node.js >= 5.x.x          | `node -v`     | [nodejs.org](http://nodejs.org/)                |
| gulp >= 3.9               | `gulp -v`     | `npm install -g gulp`                           |
| Bower >= 1.5.x            | `bower -v`    | `npm install -g bower`                          |
| Composer >= 1.0.0-alpha10 | `composer -V` | [getcomposer.org](http://getcomposer.org)       |

## Installation

* Download a pre-complied version of the dev branch: [Download Zip](http://tofino.lambdacreatives.com/tofino.zip).
* Download the latest [tagged release](https://github.com/lambdacreatives/tofino/releases).
* Clone the git repo and run `bin/setup.sh` (from your dev machine).

## Features

* [Bootstrap 4](http://getbootstrap.com/) (Pre-release)
* Multilingual ready
* Responsive
* Theme Options Panel ([Option Tree](https://github.com/valendesigns/option-tree))
	* Admin login screen logo
	* Google Analytics
	* Social links
	* Sticky menu
	* Sticky footer
	* Left/Center/Right menu positions
	* Telephone number
	* Email address
	* Company number
	* Footer text
	* Notification text / EU Cookie notice with top/bottom positions
	* Contact form with [Google reCaptcha](https://www.google.com/recaptcha) and custom email template
	* Maintenance mode
	* jQuery in footer
	* Critical CSS (with loadCSS function)
	* [Theme Tracker](https://github.com/lambdacreatives/tracker)
* [DOM-based routing](http://goo.gl/EUTi53)
* [SCSS](http://sass-lang.com/)
* [Gulp](http://gulpjs.com/) build script
	* Includes [eslint](https://github.com/eslint/eslint) and [PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
	* Use `gulp help` for a full task list with descriptions
* [Bower](http://bower.io/) for front-end package management
* [Composer](https://getcomposer.org/) for PHP package management
* [TGM Plugin Activation](https://github.com/TGMPA/TGM-Plugin-Activation)
* [Asset Builder](https://github.com/austinpray/asset-builder) for easy asset pipeline management
* Custom Nav-walker Bootstrap 4 ready
* [Relative URLs](https://codex.wordpress.org/Function_Reference/wp_make_link_relative)
* Namespaced functions
* Auto post type / slug based template routing
* SVG Sprite Shortcode `[svg sprite="my-sprite-icon"]`
* SVG Sprite helper for templates `svg('sprite-name')` or `svg(['sprite'=>'sprite-name'])`

## Documentation

Docs are provided by README.md files in each directory.

### Shortcodes

The following shortcodes are available as shortcodes in Wordpress content as well as functions in your template files.

* `svg` - Generate SVG sprite code for files from assets/svgs/sprites
* `copyright` - Generate copyright string, probably for use in the footer.
* `social_icons` - Generate a `<ul>` from the social media links. The SVG sprite name is generated by sluggifying the Title attribute.
* `option` - Get a theme option.

## Contributing

Updates and pull requests should be done on the dev branch.

New features should be done in a separate branch and sent as a pull request.

Nothing should be merged into the master branch until it has been tested on dev and (preferably) approved by all devs.

The dev branch is automatically deployed to http://tofino.lambdacreatives.com so you can test there.

No breaking changes except at major versions.

## Deployment

We use [Deploybot](https://deploybot.com). The deployment VM is issued the following commands:

```
composer install --no-dev
bower install
npm install npm -g
npm install --loglevel error
gulp --production
```

The following files and directories are excluded from being uploaded:

```
assets
bin
bower_components
gulp
node_modules
tests
.eslint
.gitattributes
.sass-lint.yml
.travis.yml
bower.json
composer.json
composer.lock
gulpfile.js
package.json
phpunit.xml
ruleset.xml
**/*.md
```
