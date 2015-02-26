# How to compile PHP from git

First: grab the source code of PHP, and check out the branch that you are interested in.  If this is your first time, don't worry, we won't be overwriting the default location of where PHP is installed on your operating system - this will be a separate build.

Before we begin, we need to create the configure files, so begin by running:

```
./buildconf
```

Now we have the configure file, we'll go ahead configure the source, but with a prefix so that it'll be installed into a separate directory and not interfere with anything. Make a command like this with your path in:

```
./configure --prefix=/path/to/phpdev/php
```

Now we're all set and we can compile the code and install it to the related location:

```
make
make install
``

The make step builds the binaries and the make install step moves them to the correct location - so you may need to sudo make install if your user doesn't have write permission to the location you set in the prefix earlier on.  At this point, you're done!  Check it works:

```
/path/to/phpdev/php/bin/php -v
```

This should show you what version of PHP you just built.

