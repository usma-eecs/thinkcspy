How to Think Like a Computer Scientist: Interactive Edition
IT105 Introduction to Computer Science
==============================================================================

This project began with the original How to Think Like a Computer Scientist text by Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris  Meyers, and Dario Mitchell.  Since 2011 Brad Miller, David Ranum, Barbara Ericson, Mark Guzdial, and many others have built on the text making it interactive.

Programming is not a "spectator sport".  It is something you do,
something you participate in. It would make sense, then,
that the book you use to learn programming should allow you to be active.
That is our goal.

This book is meant to provide you with an interactive experience as you learn
to program in Python.  You can read the text, watch videos,
and write and execute Python code.  In addition to simply executing code,
there is a unique feature called 'codelens' that allows you to control the
flow of execution in order to gain a better understanding of how the program
works.

.. image:: http://bnmnetp.me:8088/buildStatus/icon?job=thinkcspyBuild

Getting Started
===============

We have tried to make it as easy as possible for you to build and use this book.  

1. You can see and read this book online at `interactivepython.org <http://interactivepython.org/runestone/static/thinkcspy/index.html>`_

2.  You can build it and host it yourself in just a few simple steps:

    1.  ``pip install -r requirements.txt``  -- Should install everything you need
    2.  ``runestone build`` -- will build the html and put it in ``./build/thinkcspy``
    3.  ``runestone serve``   -- will start a webserver and serve the pages locally from ``./build/thinkcspy``

IT105 Specific Update Guidance
==============================

The master is tied directly to the production environment on `Runestone Academy <https://runestone.academy/runestone/static/AY182_IT105/index.html>`_. Everytime a new commit occurs for the master a Jenkins server updates the production site within about 30 minutes. The master is currently locked so only LTC Tom Babbitt has the ability to push. Assistance with content and updates to make the book better are appriciated. Please do the following to assist.

1. Fork this repository.

2. Follow the instructions above to install.

3. Only modify content in the specifed directories below **(Any other changes will effect the thinkcspy course)**:

   1. ``ICE``
   2. ``Communications``
   3. ``IT105Resources``
   4. All new directories associated with IT105 will follow the naming convention of ``IT105_XXXX``

4. Coordinate with LTC Babbitt to merge and push to master.


