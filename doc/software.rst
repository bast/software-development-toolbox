

Software that you should install prior to the course
====================================================


All exercises will be done on your laptop. You can also run them on your remote
desktop via your laptop. We will not have access to other (local) computing resources.


Alternative 1: You install the software directly on your laptop or remote desktop
---------------------------------------------------------------------------------

Disclaimer: These instructions are written
by a Linux user. Instructions for Windows and Mac OS X are
untested (please submit corrections via pull requests).

We will need:
  - Shell (bash or other shell that you like better)
  - Text editor (vi or vim or emacs or nano or atom or your favourite editor; if you
    haven't used any of these before, pick the one you can exit without killing the terminal;
    you can exit vi and vim with ":q!", emacs with "CTRL-X CTRL-C", and nano with "CTRL-X")
  - Python
  - Python packages (Sphinx, Jupyter notebook, pytest); we recommend to install these either using Anaconda or using Virtualenv
  - Git
  - Compilers: gfortran, gcc, g++ (depending on whether you use Fortran or C or C++)
  - GDB
  - Make
  - CMake: http://www.cmake.org
  - Valgrind
  - Meld or Diffuse

For Anaconda, please use the 2.7 version: https://www.continuum.io/downloads

If you prefer Virtualenv over Anaconda, please follow
http://docs.python-guide.org/en/latest/dev/virtualenvs/.  Note that you should
not try to install both.

For Mac OS X we recommend installing packages via Homebrew: http://brew.sh (use
``$ brew search <package>``). But if you like MacPorts better, that should work, too.
If you are not a sudoer, Homebrew is a better option than MacPorts. Or so I heard.

On Linux we recommend to install cmake, gfortran, gcc, g++, and git via
standard package installers (apt-get or yum or pacman or your favourite
installer). Sphinx can be installed via standard package installers although in
the long run it is convenient to install Python packages using Virtualenv.

For troubleshooting on Windows we recommend to use this good resource:
https://github.com/swcarpentry/workshop-template/wiki/Configuration-Problems-and-Solutions.


How you can verify that the installation worked
-----------------------------------------------

[I really do not know how this looks on Windows]

**Bash**

::

  $ bash --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU bash, version 4.3.42(1)-release (x86_64-unknown-linux-gnu)
  Copyright (C) 2013 Free Software Foundation, Inc.
  License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>

  This is free software; you are free to change and redistribute it.
  There is NO WARRANTY, to the extent permitted by law.

**Text editor**

Open a file and edit it. If this works, all is good.

**Python**

Open a Python shell. It should look like this (version might be different; Python 2 is good enough)::

  $ python

  Python 3.5.1 (default, Dec  7 2015, 12:58:09)
  [GCC 5.2.0] on linux
  Type "help", "copyright", "credits" or "license" for more information.
  >>>

You get out of it with CTRL-D.

**Sphinx**

::

  $ sphinx-quickstart --version

Should produce (don't worry about exact version, just make sure you don't see an error)::

  Sphinx v1.3.4

**Jupyter notebook**

::

  $ jupyter-notebook --version

Should produce (don't worry about exact version, just make sure you don't see an error)::

  4.1.0

**pytest**

::

  $ py.test --version

Should produce (don't worry about exact version, just make sure you don't see an error)::

  This is pytest version 2.8.5, imported from /foo

**Git**

::

  $ git --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  git version 2.7.0

Before you start using any Git commands,
We strongly suggest switching the global editor to the one you know how to exit.
This should do the trick::

  $ git config --global core.editor emacs # or vim or something else

**GFortran**

::

  $ gfortran --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU Fortran (GCC) 5.3.0
  Copyright (C) 2015 Free Software Foundation, Inc.

  GNU Fortran comes with NO WARRANTY, to the extent permitted by law.
  You may redistribute copies of GNU Fortran
  under the terms of the GNU General Public License.
  For more information about these matters, see the file named COPYING

**GCC**

Check output of ``gcc --version``.

**G++**

Check output of ``g++ --version``.

**GDB**

::

  $ gdb --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU gdb (GDB) 7.10.1
  Copyright (C) 2015 Free Software Foundation, Inc.

**Make**

::

  $ make --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU Make 4.1
  Built for x86_64-unknown-linux-gnu
  Copyright (C) 1988-2014 Free Software Foundation, Inc.
  License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
  This is free software: you are free to change and redistribute it.
  There is NO WARRANTY, to the extent permitted by law.

**CMake**

::

  $ cmake --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  cmake version 3.4.1

  CMake suite maintained and supported by Kitware (kitware.com/cmake).

**Valgrind**

::

  $ valgrind --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  valgrind-3.11.0

**Meld or Diffuse**

To test it create two files which are similar and then compare them
with Meld or Diffuse::

  $ meld file1 file2


Alternative 2: You code in the cloud (in your browser)
------------------------------------------------------

Use this fantastic service https://c9.io and create a workspace for this course.
A workspace is an Ubuntu container via Docker in which you can edit files,
install and run software.

You can install (almost) all the software we need with::

  $ virtualenv venv
  $ source venv/bin/activate
  $ pip install sphinx jupyter pytest
  $ sudo apt-get install fortran cmake
