## yotta: Build Software with Reusable Components
[![Build Status](https://travis-ci.org/ARMmbed/yotta.svg)](https://travis-ci.org/ARMmbed/yotta)

Yotta is a tool that we're building at [mbed](https://mbed.org), to make it easier to build better software written in C, C++ or other C-family languages. It's still early in development, so if you have questions/feedback or issues, please [report them](https://github.com/ARMmbed/yotta/issues).

### Quick Installation
To use yotta, you need:

 * yotta itself (yotta is written in [python](https://www.python.org/downloads/release/python-278/), and installed using [pip](http://pip.readthedocs.org/en/latest/installing.html))
 * [CMake](http://www.cmake.org/download/)
 * a compiler

**To install yotta itself**, download the latest [release tarball](https://github.com/ARMmbed/yotta/releases), then run:
``` bash
sudo pip install -U setuptools
sudo pip install ./path/to/yotta-a.b.c.tar.gz
```
You may need to first install [Python 2.7](https://www.python.org/downloads/release/python-278/) and [pip](http://pip.readthedocs.org/en/latest/installing.html), if you do not already have them.

**Install CMake** from the [CMake download page](http://www.cmake.org/download/), or using your system's package manager. Make sure to check the option in the installer to add it to your path. 

Which compiler you need depends on whether you're building programs for your host system, or cross-compiling them run on an embedded device:

 * to cross-compile, install [arm-none-eabi-gcc](https://launchpad.net/gcc-arm-embedded/+download).
 * to compile natively on OS X, [install Xcode](https://developer.apple.com/xcode/downloads/), including the command-line tools.
 * to compile natively on Linux, install clang with your system's package manager.

Further information on installing yotta for different platforms can be found on the [documentation site](http://docs.yottabuild.org/yotta/installing.html).

### Get Started!
The best way to get started is to [follow the tutorial](http://docs.yottabuild.org/tutorial/tutorial.html).

### What `yotta` does
yotta downloads the software components that your program depends on (it's similar in concept to npm, pip or gem). To install a new module, you run `yotta install <modulename>`, and yotta will install both the module you've specified and any of its dependencies that you don't already have installed.

To really understand how yotta works, you should install yotta (see above), then [follow the tutorial](http://docs.yottabuild.org/tutorial/tutorial.html).

### Further Documentation
For further documentation see the [yotta docs](http://armmbed.github.io/yotta/) website.

### Tips
 * `yt` is a shorthand for the `yotta` command, and it's much quicker to type!
 * yotta is strongly influenced by [npm](http://npmjs.org), the awesome node.js software packaging system. Much of the syntax for module description and commands is very similar.

### License
yotta is licensed under Apache-2.0
