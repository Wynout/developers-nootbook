# Ruby

## RubyGems
[http://rubygems.org/](http://rubygems.org/)

[RubyGems is a package manager](http://en.wikipedia.org/wiki/RubyGems) for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries (in a self-contained format called a "gem"), a tool designed to easily manage the installation of gems, and a server for distributing them. It is analogous to EasyInstall for the Python programming language. RubyGems is now part of the standard library from Ruby version 1.9.

## Guard
* [http://rubydoc.info/gems/guard/frames](http://rubydoc.info/gems/guard/frames)
* [https://github.com/guard/guard](https://github.com/guard/guard)

Guard is a command line tool to easily handle events on file system modifications.

* Automatic Sass compilation on update
* Automatic CoffeeScript compilation on updaye
* Live reloading: automatically injecting style into the browser without reloading, on update
* JavaScript concat multiple .js into one file
* Uglify, minify JavaScript

### Installation
* [net Tuts+ course :: Guard is Your Best Friend](http://net.tutsplus.com/tutorials/tools-and-tips/guard-is-your-best-friend/)
* [https://github.com/guard/guard#readme](https://github.com/guard/guard#readme)

* Install Ruby ([Ruby 1.9](http://lenni.info/blog/2011/12/installing-ruby-1-9-2-on-ubuntu-11-10-oneric-ocelot-without-using-rvm/#uninstall) or 2.0 or higher)
* Install Ruby Gems

```sh
$ sudo gem install guard
```
>$ sudo gem install ([rb-fsevent](https://github.com/nex3/rb-inotify) for OS X) or ([rb-inotify](https://github.com/nex3/rb-inotify) for Linux) or ([rb-fchange](https://github.com/stereobooster/rb-fchange) for Windows)

```sh
$ sudo gem install guard-sass
```

```sh
$ sudo gem install guard-coffeescript
```

```sh
$ sudo gem install guard-livereload
```

```sh
$ sudo gem install guard-concat
```

```sh
$ sudo gem install guard-uglify
```

* Make sure NodeJS is installed with (for example on Ubuntu)

```sh
$ sudo apt-get install nodejs
```

* Install Live Reload browser extensions.(found [here](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-))


### Initialize Guard in your project folder
```sh
$ guard init
```

or

```sh
$ guard init "gem, see above"
```

### (optional) Fix for looping guard uglify and concat on update
I fixed this in my Guardfile. I have added a second guard concat for preventing uglify to go in a loop.

```sh
$ cat Guardfile
```

		# A sample Guardfile
		# More info at https://github.com/guard/guard#readme

		# Sass input and output folder
		guard 'sass', :input => 'sass', :output => 'css'

		# CoffeeScript input and output folder
		guard 'coffeescript', :input => 'coffee', :output => 'js'

		# This will concatenate the JavaScript files specified in :files to js/concatenated.js
		# The second concat is to prevent uglify to go in a loop, ugly solution, anybody know a better solution?
		guard :concat, type: "js", files: %w(main module), input_dir: "js", output: "js/concatenated"
		guard :concat, type: "js", files: %w(main module), input_dir: "js", output: "js/minified"

		# guard :concat, type: "css", files: %w(), input_dir: "public/css", output: "public/css/all"

		guard 'uglify', :destination_file => "js/minified.js" do
		  watch 'js/concatenated.js'
		end

		# Watch these extensions and perform livereload when file is updated
		guard 'livereload' do
		  watch(%r{.+\.(css|html|js)$})
		end



[Table of Contents](TABLE-OF-CONTENTS.md#ruby)

---------------------------



