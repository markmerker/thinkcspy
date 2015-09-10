..  Copyright (C)  Brad Miller, David Ranum
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. meta::
   :description: A modified interactive version of How to Think Like a Computer Scientist.  This version, rather than being a standalone text, is to be used in conjunction with classroom lectures and exercises.
   :keywords: python, turtle graphics, computer science

.. raw:: html

   <h1 style="text-align: center">How to Think Like a Computer Scientist</h1>
   <h3 style="text-align: center">Learning Python: Special Classroom Edition for LPS </h3>

.. role:: biglink

.. raw:: html

    <style> .biglink {color:blue; font-weight: bold; font-size: 300%; } </style>





Welcome
-------------------------------------

Welcome.  This class is going to teach you the Python Programming language.   Python is a powerful language, which is fairly easy to learn and use.  It is also a language that is used by professional programmers all over the industry.
This Interactive book is designed to be used in conjunction with classroom lectures and exercises.  It will also be where you do some of your homework exercises.

This version of the book has been modified especially for Oakland LPS.  Learn about the creators of this book below.

To get started go to the

:ref:`t_o_c`    
----------------

 
But before you go, check out the kind of program you will soon be writing by pressing on "Show".

.. reveal:: lps-front-rev1
    :showtitle:Show Sample Program
    :hidetitle:Hide Sample Program

   -  Click the **"Run"** button to draw the picture
   -  Click Show/Hide Code button to see the python code.
   -  On line 7: change ``numTurtles = 10`` to ``numTurtles = 6`` and the press Run.

   .. activecode:: lps-front-code-1
       :above:
       :hidecode:
       :nocodelens:

       import turtle
       import random

       def main():
           tList = []
           head = 0
           numTurtles = 10
           wn = turtle.Screen()
           wn.setup(500,500)
           for i in range(numTurtles):
               nt = turtle.Turtle()   # Make a new turtle, initialize values
               nt.setheading(head)
               nt.pensize(2)
               nt.color(random.randrange(256),random.randrange(256),random.randrange(256))
               nt.speed(10)
               wn.tracer(30,0)
               tList.append(nt)       # Add the new turtle to the list
               head = head + 360/numTurtles

           for i in range(100):
               moveTurtles(tList,15,i)

           w = tList[0]
           #w.up()
           #w.goto(0,40)
           #w.write("How to Think Like a ",True,"center","40pt Bold")
           #w.goto(0,-35)
           #w.write("Computer Scientist",True,"center","40pt Bold")

       def moveTurtles(turtleList,dist,angle):
           for turtle in turtleList:   # Make every turtle on the list do the same actions.
               turtle.forward(dist)
               turtle.right(angle)

       main()

|

Some Handy Links
-----------------------

* Get an overview of the features in this book  `Click Here </runestone/static/overview/overview.html>`_
* To get help moving around the book:  :ref:`quick_help`

|


About this Book and Project
-------------------------------------

This interactive book is a product of the `Runestone Interactive <http://runestoneinteractive.org>`_ Project at Luther College, led by `Brad Miller <http://reputablejournal.com>`_ and David Ranum.  There have been many contributors to the project.  Our thanks especially to the following:

* This book is based on the `Original work <http://www.openbookproject.net/thinkcs/python/english2e/>`_ by:  Jeffrey Elkner, Allen B. Downey, and Chris Meyers
* Activecode based on `Skulpt <http://skulpt.org>`_
* Codelens based on `Online Python Tutor <http://www.pythontutor.com>`_
* Many contributions from the `CSLearning4U research group <http://home.cc.gatech.edu/csl/CSLearning4U>`_ at Georgia Tech.
* ACM-SIGCSE for the special projects grant that funded our student Isaac Dontje Lindell for the summer of 2013.

The Runestone Interactive tools are open source and we encourage you to contact us, or grab a copy from GitHub if you would like to use them to write your own resources.

* Visit our `Facebook page <https://www.facebook.com/RunestoneInteractive>`_


.. toctree::
   :hidden:

   index
   navhelp

