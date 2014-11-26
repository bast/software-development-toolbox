

Get comfortable with Git
========================


Basic init-add-commit workflow
------------------------------

Initialize an empty Git repository, add some source code or text and commit few
changes. Use ``git status`` a lot.  Test ``git log``, ``git grep``, ``git
diff``. Create files that you want ignored by Git.  Make Git ignore these
files.


Git branching game
------------------

Try to solve basic exercises in "Main" and "Remote":
http://pcottle.github.io/learnGitBranching/

You decide how far you want to get and which topics
are most relevant to your work.


Fork and pull-request
---------------------

Make a fork of https://github.com/rbast/software-development-toolbox.
Then inspect ``index.rst`` and ``doc/`` and compare
them to http://toolbox.readthedocs.org.
It will be then hopefully quickly clear how they map to each other.

Commit a small change to the repository. Either improve
the software installation section or find a bug or typo or suggest
a fun exercise. Then submit the change as pull-request.

We will then together inspect the pull-requests and integrate
them to the main repository.


Update forked repository
------------------------

After we have finished and reviewed the fork and pull-request exercise you will
learn to update your forked repository with the combined changes integrated to
the upstream repository.  We may need to resolve conflicts.


Git bisect exercise
-------------------

Clone the https://github.com/rbast/bisect-me exercise.
The repository consists of one single script which approximately calculates pi::

  $ python get_pi.py

It should produce 3.14159241097 but it does not. It produces 3.26459241097 using
the last commit.

The script calculates pi using the 100 first terms of the Nilakantha series. At
each commit, the 100 terms are reshuffled. At some point within the 1000 first
commits, an error was introduced. The only thing we know is that the first
commit worked correctly.

Use ``git bisect`` to find the commit which broke the computation.

Bonus: write a script that checks for a correct result and use ``git bisect
run`` to find the offending commit automatically.

The motivation for this exercise is to be able to do archaeology with Git on a
source code where the bug is difficult to see visually.  Once you find the
offending commit, it is often much easier to figure out why it is broken (in
this particular example it won't help us but in reality mastering ``git
bisect`` is a huge time saver).
