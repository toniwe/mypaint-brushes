mypaint-brushes - MyPaint brushes
=================================

Brushes used by MyPaint and other software using libmypaint.

This data package is versionned. This are the brushes to be used by
libmypaint 1.x, not the ones to be used by current development version
(libmypaint 2.x; which has no releases to the day of writing).

Building
---------

mypaint-brushes package can be installed as a typical autotools build:

> ./configure --prefix=/some/prefix && make && make install

See also `INSTALL` file.

There are also historical scons scripts, but they work only with scons
2.x (and in particular not newer scons 3, based on Python 3):

> scons prefix=/your/application/install/prefix # Normal build
> scons -h                                      # Show build options

Using the brushes with pkg-config
---------------------------------

If your application needs libmypaint 1.x brushes, you can make the
module "mypaint-brushes-1.0" a dependency with pkg-config.

For a C/C++ program, the CFlags generated by pkg-config will define the
macro MYPAINT_BRUSHES_DIR, usable in your code in order to get the path
for all mypaint default brushes.

For programs in other languages, you can use the variable `brushesdir`
to get the same information with pkg-config and insert this value in
your program in the relevant way.

> pkg-config --variable=brushesdir mypaint-brushes-1.0
