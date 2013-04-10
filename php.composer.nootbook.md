
# Composer

## Sources
* [http://getcomposer.org/](http://getcomposer.org/)
* [Using composer in CakePHP 3.0](http://mark-story.com/posts/view/using-composer-in-cakephp-3-0)
* Packages are generally published on the [packagist](https://packagist.org/)
* [Composer on Github](https://github.com/composer/composer/blob/master/README.md)
* [Easy package management with composer](http://net.tutsplus.com/tutorials/php/easy-package-management-with-composer/)

Composer is a tool for dependency management in PHP.

It allows you to declare the dependent libraries your project needs and it will install them in your project for you.

It borrows many ideas from npm and uses basic json files for package definitions.
Composer packages are generally published on the packagist, but can also be published & installed from other servers

-------------------

## Install Composer globally

```sh
$ curl -sS https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
```
Then, just run `composer` instead of `php composer.phar`

## Update a phar install with the latest version

```sh
$ composer self-update
```

[Table of Contents](TABLE-OF-CONTENTS.md#)

-------------------


## Composer Courses | Tutorials | Screencasts
* [tuts+ Hands-On: Build a Practical Web Application with Laravel](https://tutsplus.com/course/hands-on-building-a-practical-web-application-with-laravel/)
* https://tutsplus.com/course/laravel-essentials/

-------------------

## Word definition list
### phar
>The [phar](http://www.php.net/manual/en/intro.phar.php) extension provides a way to put entire PHP applications into a single file called a "phar" (PHP Archive) for easy distribution and installation.
In addition to providing this service, the phar extension also provides a file-format abstraction method for creating and manipulating tar and zip files through the PharData class, much as PDO provides a unified interface for accessing different databases.
Unlike PDO, which cannot convert between different databases, Phar also can convert between tar, zip and phar file formats with a single line of code.
