# Ruby

## RubyGems
[http://rubygems.org/](http://rubygems.org/)

[RubyGems is a package manager](http://en.wikipedia.org/wiki/RubyGems) for the Ruby programming language that provides a standard format for distributing Ruby programs and libraries (in a self-contained format called a "gem"), a tool designed to easily manage the installation of gems, and a server for distributing them. It is analogous to EasyInstall for the Python programming language. RubyGems is now part of the standard library from Ruby version 1.9.

## Guard
* [http://rubydoc.info/gems/guard/frames](http://rubydoc.info/gems/guard/frames)
* [https://github.com/guard/guard](https://github.com/guard/guard)

Guard is a command line tool to easily handle events on file system modifications.

	* automatic Sass compilation on save
	* automatic CoffeeScript compilation on save
	* Live reloading: automatically injecting style into the browser without reloading, on save
	* Javascript concat multiple .js into one file
	* Uglify----minify javascript

### Installation
[source Tuts+](http://net.tutsplus.com/tutorials/tools-and-tips/guard-is-your-best-friend/)

* Install Ruby
* Install Ruby Gems
		$ gem install guard
		$ gem install rb-fsevent
		$ gem install guard-sass
		$ gem install guard-coffeescript
		$ gem install guard-livereload
		$ gem install guard-concat
		$ gem install guard-uglify
		# (or gem install guard rb-fsevent guard-sass guard-coffeescript guard-livereload guard-concat guard-uglify)

* Install Live Reload browser extensions.(found [here](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions-))

* Make sure NodeJS is installed with
>$ apt-get install nodejs


## Initialize Guard in your project folder

>$ guard init


[Table of Contents](TABLE-OF-CONTENTS.md#ruby)

---------------------------



