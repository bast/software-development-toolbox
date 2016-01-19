

Get comfortable with Git
========================

You can work on the exercises "out of order" - in the order
that is most interesting/relevant for you.


Basic init-add-commit workflow
------------------------------

Initialize an empty Git repository, add some source code or text and commit few
changes. Use ``git status`` a lot.  Test ``git log``, ``git grep``, ``git
diff``. Experiment with the staging area with ``git add`` and verify how ``git
diff`` behaves with staged changes.  Create files that you want ignored by Git.
Make Git ignore these files. Create branches, switch between them, merge them,
delete them.


Git branching game
------------------

Try to solve basic "Main" and "Remote" exercises in
http://pcottle.github.io/learnGitBranching/. You decide how far you want to
get and which topics are most relevant for your work.


Practice working with remotes (on a local machine)
--------------------------------------------------

- Create a normal Git repository on your laptop (repo A).
- Create, add, and commit a README file or an example source file or script.
- Clone it into a bare repository (repo B).
- Clone the bare into another non-bare repository (repo C), everything still on your computer.
- Have a look at ``git remote -v`` in repo C.
- Have a look at ``git remote -v`` in repo B.
- Have a look at ``git remote -v`` in repo A.
- Add the bare repo B as remote in A.
- Exercise communicating changes between the two non-bare clones (A and C).
- Verify that ``origin`` is just a label by pushing directly to the full path.
- Create a GitHub project (without auto-creating ``README``, ``LICENSE``, or ``.gitignore``).
- Change ``origin`` to now point to GitHub and push the entire ``master`` branch from one our your local
  repos into it.


Collaborative GitHub workflow
-----------------------------

https://github.com/bast/github-workflow-exercise


Git bisect exercise
-------------------

https://github.com/bast/bisect-me
