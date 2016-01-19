

Test-driven development
=======================

We will do this exercise in pairs. Not only we will learn how to do
test-driven development, but we will also exercise collaborative GitHub
workflow, and get to know two great services for automated testing (Travis) and
code coverage analysis (Coveralls).

First find a partner who speaks the same programming language as you.
Then proceed as follows (both of you, separately):
- Create a GitHub project for this exercise.
- Sign in to https://travis-ci.org and https://coveralls.io with your GitHub account and enable there your new GitHub project.
- Create two or three unit tests for functions which do not exist yet.
- Do not implement the functions, only their tests and stubs of the functions.

Example (Python; the function get_word_lengths currently fails):
.. code-block:: python

  def get_word_lengths(s):
      """
      Returns a list of integers representing
      the word lengths in string s.
      """
      return None


  def test_get_word_lengths():
      text = "Three tomatoes are walking down the street"
      assert get_word_lengths(text) == [5, 8, 3, 7, 4, 3, 6]

Then:
- Check that the test fails (since the function is not implemented/finished).
- Commit the function and its test.
- Create a .travis.yml file based on provided examples (below) and commit it.
- Push the tests and function stubs to GitHub and verify that the tests fail on Travis.

Now your programming partner forks your repository and you fork hers/his. Then:
 - Fix the function/routine until the test(s) pass(es).
 - Commit and push the working function/routine.
 - Check and discuss the test history on https://travis-ci.org.
 - Check and discuss the test coverage on https://coveralls.io.
 - Iterate and refine.

When you are finished, submit your work as pull request and
your programming partner will review and possibly accept the changes.

Examples that you can use as a starting point:
 - `Python example using pytest <https://github.com/bast/pytest-demo>`_
 - `C/C++ example using Google Test <https://github.com/bast/gtest-demo>`_
 - `Fortran example using pFUnit <https://github.com/bast/pfunit-demo>`_
