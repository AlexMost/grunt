# grunt [![Build Status](https://secure.travis-ci.org/gruntjs/grunt.png?branch=devel)](http://travis-ci.org/gruntjs/grunt)
Grunt is a task-based command line build tool for JavaScript projects.

_Grunt is currently in beta. While I'm already using it on multiple projects, it might have a minor issue or two. And things might change before its final release, based on your feedback. Please try it out in a project, and [make suggestions][issues] or [report bugs][issues]!_

## Getting started
Be sure to read the [getting started guide](/gruntjs/grunt/blob/master/docs/getting_started.md), which is a complete guide to configuring grunt for your project. In addition, check out the [example Gruntfiles](/gruntjs/grunt/blob/master/docs/example_gruntfiles.md) which highlight a number of fairly common configurations.

## Custom tasks
In addition to the built-in tasks, you can create your own tasks. Don't like a built-in task's default behavior? Override it. Check out the [grunt API documentation](/gruntjs/grunt/blob/master/docs/api.md) and the [built-in tasks source](/gruntjs/grunt/blob/master/tasks) for everything you need to know about creating custom tasks.

## Documentation
Take a look at the [documentation table of contents][docs] for all the things.

## Why does grunt exist?
Doing all this stuff manually is a total pain, and building all this stuff into a gigantic Makefile / Jakefile / Cakefile / Rakefile / ?akefile that's maintained across all my projects was also becoming a total pain. Since I always found myself performing the same tasks over and over again, for every project, it made sense to build a task-based build tool.

Being primarily a JavaScript developer, I decided to use [Node.js][node] and [npm][npm] because the dependencies I most care about ([JSHint][jshint] and [UglifyJS][uglify]) were already npm modules. That being said, while Node.js was designed to support highly-concurrent asynchronous-IO-driven web servers, it was clearly NOT designed to make command-line build tools. But none of that matters, because grunt works. Just install it and see.

## Installing grunt

Grunt is available as an [npm][npm] module. If you install grunt globally via `npm install -g grunt`, it will be available for use in all of your projects. Once grunt has been installed, you can type `grunt --help` at the command line for more information. And if you want to see grunt "grunt" itself, cd into grunt's directory and type `grunt`

_Note: in Windows, you may need to run grunt as `grunt.cmd`. See the [FAQ](/gruntjs/grunt/blob/master/docs/faq.md) for more Windows-specific information._

For projects already using grunt, you're done. Otherwise, if you're adding grunt to an existing project or starting from scratch, check out the [getting started guide](/gruntjs/grunt/blob/master/docs/getting_started.md), which is a complete guide to configuring grunt for your project.

## Release History
_(Until v1.0.0, this will only be updated when major or breaking changes are made)_

* 2012/06/25 - v0.3.10 - Updating a few dependencies to work with node 0.8.x (0.6.x should still work).
* 2012/04/18 - v0.3.9 - The min task (via the uglify helper) now appends a semicolon to the end of the generated source.
* 2012/04/06 - v0.3.8 - Init template tweaks. Anchor links added to docs, along with grunt-internal docs task to generate them. The watch task now supports multiple targets with separate wildcards and tasks. Locally-installed grunt will override global grunt even when run from global "grunt" script.
* 2012/04/01 - v0.3.7 - Tweaked the behavior of the init template `exports.warnOn` property and added more init template documentation. Fixed duplicate PhantomJS debug output in qunit task. Added useful nodeunit and qunit comments into init template generated test .js files.
* 2012/03/28 - v0.3.6 - Fixed a `--help` screen issue, a few grunt plugin related issues, and attempted to improve the overall grunt plugin docs and API.
* 2012/03/27 - v0.3.5 - Fixed a handful of weird Windows issues. Changed default m/d/yyyy dates to yyyy-mm-dd ISO 8601. Fixed some init task bugs, docs errata, and added a lot more content to the init task docs.
* 2012/03/26 - v0.3.3 - Added a "gruntfile" init template. Create a basic Gruntfile in seconds with `grunt init:gruntfile`. A few other minor fixes.
* 2012/03/25 - v0.3.2 - Init tasks can now specify a file matching wildcard for the initial "files exist" warning. The jQuery init template now has jQuery 1.7.2. Fixed a bug in the `task.expand*` methods.
* 2012/03/25 - v0.3.1 - Added a few methods. Substantially reworked the init task and templates.
* 2012/03/23 - v0.3.0 - Too many changes to list. But in brief: completely reorganized the API, removed all globals, added docs and examples for nearly everything, built a preliminary plugin system (that still needs to be tested). PLEASE RTFM OK? THX U.
* 2012/02/03 - v0.2.14 - Added a server task (which starts a static webserver for your tasks). The qunit task now uses PhantomJS instead of Zombie.js (4768 of 4971 jQuery unit test pass, neat), and supports both file wildcards as well as http:// or https:// urls. (static webserver, anyone?). Grunt should no longer "hang" when done.
* 2012/01/29 - v0.2.5 - Added a "qunit" task as well as an init "jquery" template (as of now, there are also "node" and "commonjs" init templates).
* 2012/01/22 - v0.2.1 - Removed handlebars, templates are universally handled by underscore now. Changed init task template tags from <% %> to {% %}. Banners beginning with /*! will no longer be stripped.
* 2012/01/22 - v0.2.0 - Added "init" task with a sample template, reworked a lot of code. Hopefully it's backwards-compatible.
* 2012/01/11 - v0.1.0 - Initial release.

## License
Copyright (c) 2012 "Cowboy" Ben Alman  
Licensed under the MIT license.  
<https://github.com/gruntjs/grunt/blob/master/LICENSE-MIT>


[docs]: /gruntjs/grunt/blob/master/docs/toc.md
[docs-init]: /gruntjs/grunt/blob/master/docs/task_init.md
[issues]: /gruntjs/grunt/issues

[node]: http://nodejs.org/
[npm]: http://npmjs.org/
[jshint]: http://www.jshint.com/
[uglify]: https://github.com/mishoo/UglifyJS/
[nodeunit]: https://github.com/caolan/nodeunit
[qunit]: http://docs.jquery.com/QUnit
[phantom]: http://www.phantomjs.org/
