# smake r1045
  a program analysis preparation tool for C programs made with GNU Make

smake observes the build process driven by make(1), and derives the
standalone, preprocessed form of the source code that makes up each
C program linked during the process.  smake creates a directory
"sparrow/", where you can perform program analyses with make(1).

You can instantly start your program analysis in three steps:
 1. Initialize "sparrow/", i.e. $AMAKEDIR.
 2. Use `smake` instead of `make` to build your programs.
 3. Use `make` under $AMAKEDIR to analyze your programs.

Usage:
 $ smake --init [<options>]
  initializes sparrow/ to handle the regular use of smake.
  If you use a special compiler (e.g. cross compiler), its type must be
  specified by appending gcc style options, e.g. `-b mips-linux -V 2.95`.

 $ smake --clean
  completely removes sparrow/.

 $ smake <parameters for make>
  runs `make [<with parameters>]` and bookkeeps $AMAKEDIR.

 $ smake ./configure
  runs `./configure` under the same environment `smake` runs.

 $ smake --help
  shows this message.

