

Create a CMake framework for a project and practice debugging with Valgrind
===========================================================================

In this exercise we will CMake-ify a project.
This is interesting for people who use Makefiles
or Autotools.

You can use the exercise time to practice CMake on your own
project(s) but we also provide a mockup project:
https://github.com/bakerjonas/vat-69.git

Your task is to:
 - Create a build system using CMake:
     - Build a shared library
     - Build and link the main program
     - Create an installer so the program can be installed properly (GNU standards)
     - Compile a parallel version with OpenMP
 - Find all bugs using Valgrind and fix them
 - Find all parallelization bugs using Helgrind (part of Valgrind)
