---
layout: post
title: "Automate Your Application Development"
quote: "Some tips on automating an application build process to accelerate the development speed."
image: false
video: false
comments: true
---

Take the time to setup a build process for your new project, you will see the benifits instantly. I've recently experimented with [Apcache Ant](http://ant.apache.org/) which is a widely known build automation software used mostly by the Java community. _I don't like Ant_. _I don't like XML_. Especially in a JavaScript project. Fortunately there are projects like [Grunt](http://gruntjs.com/) and [Gulp](http://gulpjs.com/) that are adapted to a JavaScript application stack.

# I choose Gulp
I've decided to write my apps with Gulp.

>code-over-configuration

That was the selling point. I just said that I don't like XML. Even if Ant used JSON, it wouldn't solve the problem at all. That's pretty much what Grunt is to me, a bonified Ant version for JavaScript with a JSON configuration. On the other side, Gulp provides a more functional interface that you configure by code. Isn't that what we do every day? And that's what we're good at!

# Remove the pain points of preprocessors
I write my stylesheets in LESS. I write my scripts in TypeScript. If I had to fire up the console to compile each time I modified code, I'd probably go nuts (I actually started a big project this way, and lasted about 2 days).

Preprocessors are awesome, they are less error prone and facilitate maintenance and refactorings, but they can be a pain if not automated. Fortunately, Gulp offers many included plugins for the mosts popular compiled languages and a ******load of third-party plugins are also available.

Most build tools also offer a `watch` task, that can monitor certain files or folders and run certain tasks.

# Use it
Use it to

* compile to JavaScript ([TypeScript](https://github.com/kotas/gulp-tsc), [CoffeeScript](https://github.com/wearefractal/gulp-coffee), etc.)
* compile to CSS ([LESS](https://github.com/plus3network/gulp-less), [SASS](https://github.com/dlmanning/gulp-sass), [Stylus](https://github.com/stevelacy/gulp-stylus))
* [minify](https://github.com/terinjokes/gulp-uglify) files
* [concatenate](https://github.com/wearefractal/gulp-concat) files
* run tests
* convert images to sprites stylesheets
* [lint](https://github.com/spenceralger/gulp-jshint) and check for error

The list goes on. Each of these tasks can be invoked by a file change via the file watchers.

On your next project (or current), take a little time to set up a build process. It shouldn't take you long. You will be happy to use all those fancy preprocessors and compile-to-JS languages and watch your productivity increase exponentially!


