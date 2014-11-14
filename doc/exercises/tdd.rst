

Test-driven debugging and development
=====================================

Below you find a collection of problems. Start with the ones you like in your
favourite language. You do not have to finish all and you can test own problems
instead. Each function should be separately tested.  The point here is to get
into contact with testing, continuous integration, and test coverage.

Proceed as follows:
 - Create a GitHub project for this exercise.
 - Sign in to https://travis-ci.org and https://coveralls.io with your GitHub account and enable there your new GitHub project.
 - For each problem start with an empty/mock function/routine that does not work.
 - Create a test for this function/routine using pytest or nose or Google Test or pFUnit depending on your language.
 - Check that the test fails (since the function is not implemented/finished).
 - Commit the function and its test.
 - Create a .travis.yml file based on provided examples (below) and commit it.
 - Push to GitHub.
 - Fix the function/routine until the test passes.
 - Commit and push the working function/routine.
 - Check and discuss the test history on https://travis-ci.org.
 - Check and discuss the test coverage on https://coveralls.io.
 - Iterate and refine.

Examples that you can use as a starting point:
 - `Python example using pytest <https://github.com/rbast/pytest-demo>`_
 - `C/C++ example using Google Test <https://github.com/rbast/gtest-demo>`_
 - `Fortran example using pFUnit <https://github.com/rbast/pfunit-demo>`_


Ranges with steps
-----------------

Inspired by http://learnyouahaskell.com.

Write a function/routine that receives a string and returns a list of integers, for
example::

  "[2,4..20]" -> [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
  "[3,6..20]" -> [3, 6, 9, 12, 15, 18]


Deaf Grandma
------------

Heavily inspired by https://pine.fm/LearnToProgram.

Write a deaf grandma program. Whatever you say to grandma (input), she should
respond with "HUH?! SPEAK UP, SONNY!" (output), unless you shout it (input in
all capitals). If you shout, she can hear you (or at least she thinks so) and
yells back, "NO, NOT SINCE 1938!". When you shout "BYE", she could pretend not
to hear you. You have to shout "BYE" three times in a row so that she says
"BYE".  Make sure to test your program: if you shout "BYE" three times, but not
in a row, you should still be talking to grandma.


Reverse a character string
--------------------------

Example::

  "foobar" -> "raboof"


Reverse a list of integers
--------------------------

Example::

  [1, 3, 5, 2] -> [2, 5, 3, 1]


Implement min() and max() functions
-----------------------------------

A function that returns minimum or maximum
value of a list/array.


Sum of digits
-------------

A function that returns the sum of the digits of an integer.


BADA BING!
----------

Inspired by http://learnyouahaskell.com.

Write a function that replaces each odd number greater than 10 with "BING!" and
each odd number that is less than 10 with "BADA". If a number is not odd, we
throw it out of our list.

Example::

  [1, 2, 7, 8, 10, 13] -> ["BADA", "BADA", "BING!"]


Find the right triangle
-----------------------

Inspired by http://learnyouahaskell.com.

Find a triangle that fits the following conditions:
 - One angle is 90 degrees
 - The lengths of the three sides are all integers
 - The length of each side is less than or equal to 10
 - The sum of the side lengths is equal to 24


Advanced and fun exercise: Snake game using Python curses
---------------------------------------------------------

It is fun, it is visual and it is quite easy.
