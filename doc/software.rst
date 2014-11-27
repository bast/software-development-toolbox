

Software that you should install prior to the course
====================================================

All exercises will be done on your laptop. You can also run them on your remote
desktop via your laptop. We will not have access to other (local) computing resources.

We will need:
  - Shell (bash or other shell that you like better)
  - Text editor (vi or vim or emacs or nano or your favourite editor)
  - Python
  - Sphinx http://sphinx-doc.org
  - Recommended but not mandatory: Virtualenv (http://docs.python-guide.org/en/latest/dev/virtualenvs/) or Anaconda
  - Git
  - Compilers: gfortran, gcc, g++ (depending on whether you use Fortran or C or C++)
  - CMake: http://www.cmake.org

**Update: As an alternative to individual installations
we will also provide a virtual Linux image with all software
pre-installed which you will be able to run using https://www.virtualbox.org**.

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
