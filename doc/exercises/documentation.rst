

Modern code documentation
=========================


Part 1: Sphinx-based documentation on Read the Docs
---------------------------------------------------

In this exercise we will implement a Sphinx-based documentation, host it on
GitHub and deploy it to https://readthedocs.org. This is exactly how this
page that you read right now arrives to your browser (the sources are here:
https://github.com/bast/software-development-toolbox).

- Set up a virtual environment according to http://docs.python-guide.org/en/latest/dev/virtualenvs/.
- Install Sphinx to the virtual environment.
- Run ``sphinx-quickstart`` (http://sphinx-doc.org/tutorial.html).
- Build the html and check it locally on your computer and in your browser.
- Make some changes to it and build them locally.
- Create a new GitHub project for it.
- Push the documentation sources to the new GitHub project.
- Create an account at https://readthedocs.org.
- Import the Github project you just created to Read the Docs.
- Create a post commit hook in GitHub so that changes automatically refresh the Read the Docs pages.
- Test the post commit hook by making and pushing changes to the documentation sources and verify
  that the documentation refreshes after your changes.


Part 2: Create an example project website and host it on GitHub Pages
---------------------------------------------------------------------

Create an example project website (from GitHub Pages templates or on your own)
and host it on GitHub Pages (https://pages.github.com). If you use Doxygen, try
to host Doxygen-generated documentation on GitHub Pages.
