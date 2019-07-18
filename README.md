# V8 Javascript Engine compiled files for PHP
V8JS compiled files for PHP in Ubuntu.

## Working with
* Ubuntu 18.04 or 19.04
* PHP 7.2.9

## Dependencies
```
$ sudo apt-get install build-essential curl git python libglib2.0-dev php7.2-dev
```

## Installation
```
$ cd /opt
$ git clone https://github.com/davidecesarano/phpv8js-compiled.git
```

## Compile php-v8js itself
```
$ cd /tmp
$ git clone https://github.com/phpv8/v8js.git
$ cd v8js
$ phpize
$ ./configure --with-v8js=/opt/v8 LDFLAGS="-lstdc++"
$ make
$ make test
$ sudo make install
```

## Add extension
Add `extension=v8js.so` to your php.ini file. 