

Software that you should install prior to the course
====================================================


All exercises will be done on your laptop. You can also run them on your remote
desktop via your laptop. We will not have access to other (local) computing resources.


Alternative 1: Virtualbox
-------------------------

As an alternative to individual installations
we will also provide a virtual Linux image with all software
pre-installed which you will be able to run using https://www.virtualbox.org.

This is in particular practical for Windows laptops but
it should work on virtually any platform.

- Download and install https://www.virtualbox.org
- Download the pre-installed Linux image (you will receive the download location via email)
- Extract the image (on Linux ``$ tar xvzf trusty32.tgz``)
- Start Virtualbox
- "File" -> "Import Appliance" -> select the extracted ``box.ovf`` -> "Import"
- Start the imported machine (big green arrow)
- Log in as vagrant:vagrant (using LXDE session)
- Adjust the keyboard to your layout (bottom left -> "Preferences" -> "Lxkeymap")
- Open a terminal
- Edit ``.gitconfig``


Alternative 2: You install the software directly on your laptop or remote desktop
---------------------------------------------------------------------------------

We will need:
  - Shell (bash or other shell that you like better)
  - Text editor (vi or vim or emacs or nano or your favourite editor)
  - Python
  - Sphinx http://sphinx-doc.org
  - Recommended but not mandatory: Virtualenv (http://docs.python-guide.org/en/latest/dev/virtualenvs/) or Anaconda
  - Git
  - Compilers: gfortran, gcc, g++ (depending on whether you use Fortran or C or C++)
  - CMake: http://www.cmake.org
  - Valgrind
  - IPython for those who want to experiment with it
  - Meld or Diffuse

People who have never used a compiled language and are certain that they never
will, can skip installing compilers and CMake. We have tailored exercises for
"Python-only" programmers.

Disclaimer: These instructions are written
by a Linux user. Instructions for Windows and Mac OS X are
untested.

For Mac OS X we recommend installing packages via Homebrew: http://brew.sh (use
``$ brew search <package>``). But if you like MacPorts better, that should work, too.

For Windows we recommend to follow installation instructions for the shell, text
editor, Python, and Git as provided by the Software Carpentry (we will not need
R or SQLite): http://software-carpentry.org/v5/setup.html. These are in principle
well tested.

On Linux we recommend to install cmake, gfortran, gcc, g++, and git via
standard package installers (apt-get or yum or pacman or your favourite
installer). Sphinx can be installed via standard package installers although in
the long run it is convenient to install Python packages using Virtualenv.


How you can verify that the installation worked
-----------------------------------------------

[I really do not know how this looks on Windows]

**Bash**

::

  $ bash --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU bash, version 4.2.37(1)-release (x86_64-pc-linux-gnu)
  Copyright (C) 2011 Free Software Foundation, Inc.
  License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>

  This is free software; you are free to change and redistribute it.
  There is NO WARRANTY, to the extent permitted by law.

**Text editor**

Open a file and edit it. If this works, all is good.

**Python**

Open a Python shell. It should look like this::

  $ python

  Python 2.7.3 (default, Mar 13 2014, 11:03:55)
  [GCC 4.7.2] on linux2
  Type "help", "copyright", "credits" or "license" for more information.
  >>>

You get out of it with CTRL-D.

**Sphinx**

::

  $ sphinx-quickstart

Should produce::

  Welcome to the Sphinx 1.2.3 quickstart utility.

  Please enter values for the following settings (just press Enter to
  accept a default value, if one is given in brackets).

  Enter the root path for documentation.
  > Root path for the documentation [.]:

You can abort it with CTRL-C.

**Virtualenv**

Installing a test virtualenv under ``/tmp`` should look like this::

  $ cd /tmp
  $ virtualenv env

  New python executable in env/bin/python
  Installing setuptools, pip...done.

**Git**

::

  $ git --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  git version 1.7.10.4

**GFortran**

::

  $ gfortran --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  GNU Fortran (Debian 4.7.2-5) 4.7.2
  Copyright (C) 2012 Free Software Foundation, Inc.

  GNU Fortran comes with NO WARRANTY, to the extent permitted by law.
  You may redistribute copies of GNU Fortran
  under the terms of the GNU General Public License.
  For more information about these matters, see the file named COPYING

**GCC**

Check output of ``gcc --version``.

**G++**

Check output of ``g++ --version``.

**CMake**

::

  $ cmake --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  cmake version 2.8.9

**Valgrind**

::

  $ valgrind --version

Should give you a version (like here) and not an error
(don't worry if the version is different on your system)::

  valgrind-3.7.0

**IPython**

::

  $ ipython

Should produce an output similar to this::

  Python 2.7.3 (default, Mar 13 2014, 11:03:55)
  Type "copyright", "credits" or "license" for more information.

  IPython 2.3.1 -- An enhanced Interactive Python.
  ?         -> Introduction and overview of IPython's features.
  %quickref -> Quick reference.
  help      -> Python's own help system.
  object?   -> Details about 'object', use 'object??' for extra details.

  In [1]:

You get out of it with CTRL-D.

**Meld or Diffuse**

To test it create two files which are similar and then compare them
with Meld or Diffuse::

  $ meld file1 file2
