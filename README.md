[![Build Status](https://travis-ci.org/lambdacreatives/tofino.svg)](https://travis-ci.org/lambdacreatives/tofino) [![devDependency Status](https://david-dm.org/lambdacreatives/tofino/dev-status.svg)](https://david-dm.org/lambdacreatives/tofino#info=devDependencies) [![Deployment status from DeployBot](https://lambdacreatives.deploybot.com/badge/77558060036000/47551.svg)](http://deploybot.com)

<img src="https://raw.githubusercontent.com/lambdacreatives/tofino/master/screenshot.png" alt="Tofino" width="500">

# Tofino

A WordPress starter theme for jumpstarting custom theme development.

Developed by [Daniel Hewes](https://github.com/danimalweb), [Jake Gully](https://github.com/mrchimp).

[Demo](http://tofino.lambdacreatives.com)

## Requirements

| Prerequisite              | How to check  | How to install                                  |
| ------------------------- | ------------- | ----------------------------------------------- |
| PHP >= 5.5.9              | `php -v`      | [php.net](http://php.net/manual/en/install.php) |
| Node.js >= 5.x.x          | `node -v`     | [nodejs.org](http://nodejs.org/)                |
| gulp >= 3.9               | `gulp -v`     | `npm install -g gulp`                           |
| Composer >= 1.0.0-alpha10 | `composer -V` | [getcomposer.org](http://getcomposer.org)       |

## Installation

* Download a pre-complied version of the dev branch: [Download Zip](http://tofino.lambdacreatives.com/tofino.zip).
* Download the latest [tagged release](https://github.com/lambdacreatives/tofino/releases).
* Clone the git repo and run `bin/setup.sh` (from your dev machine).

Once you have activated the theme, access Theme Options (WP Customizer) update an option and select save to commit the default values to the database.

## Features

* [Bootstrap 4](http://getbootstrap.com/) (Pre-release Alpha 2)
* Multilingual ready (WPML)
* Responsive
* Theme Options via WP Customizer (Native)
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
	* Contact form with [Google reCAPTCHA](https://www.google.com/recaptcha) and custom email templates
	* Maintenance mode
	* jQuery in footer
	* Critical CSS (with loadCSS function)
	* [Theme Tracker](https://github.com/lambdacreatives/tracker)
* [DOM-based routing](http://goo.gl/EUTi53)
* [SCSS](http://sass-lang.com/)
* [Gulp](http://gulpjs.com/) build script
	* Includes [eslint](https://github.com/eslint/eslint) and [PHP CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
	* Use `gulp help` for a full task list with descriptions
* [Composer](https://getcomposer.org/) for PHP package management
* Custom Nav-walker Bootstrap 4 ready
* [Relative URLs](https://codex.wordpress.org/Function_Reference/wp_make_link_relative)
* Namespaced functions
* Auto post type / slug based template routing
* Shortcodes
* AjaxForm handler class. Easily handle form validation and processing with Wordpress Ajax. Send submitted data via email and/or save it as post meta. Add your own custom validator / processor via a simple function hook.

## Documentation

Docs are provided by README.md files in each directory.

## Contributing

Updates and pull requests should be done on the dev branch.

New features should be done in a separate branch and sent as a pull request.

Nothing should be merged into the master branch until it has been tested on dev and (preferably) approved by all devs.

The dev branch is automatically deployed to http://tofino.lambdacreatives.com so you can test there.

No breaking changes except at major versions.

## Deployment

We use [Deploybot](https://deploybot.com). The deployment VM is issued the following commands:

```
composer install
npm install npm -g
npm install --loglevel error
gulp --production
```

The following files and directories are excluded from being uploaded:

```
assets
bin
gulp
node_modules
.eslintrc.yml
.gitattributes
.sass-lint.yml
.travis.yml
composer.json
composer.lock
gulpfile.js
package.json
ruleset.xml
**/*.md
```
