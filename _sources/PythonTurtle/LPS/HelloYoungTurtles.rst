..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. |NOTE| image:: ../GeneralIntro/LPS/Figures/pencil.png

.. role:: notetext

.. raw:: html

    <style> .notetext {color:green; font-weight: bold; font-size: 110%; } </style>

.. role:: sctnhead

.. raw:: html

    <style> .sctnhead {color:black; font-weight: bold; font-size: 140%; } </style>
    
.. qnum::
   :prefix: lps-hyt-
   :start: 1




Hello Young Turtles!
=====================


Young?  How long do turtles live?  Well, between 10 and 150 years.

The tortoise Tu'i Malila,  was presented to the Tongan royal family by the British explorer Captain Cook shortly after its birth in 1777.  It remained in the care of the Tongan royal family until its death by natural causes on May 19, 1965, at the age of 188.  (Your teacher was 15 years old at that time.)


Python Modules
----------------
There are many *modules* in Python which provide very powerful features that we can use in our  programs.  Some of these can send email or fetch web pages. Others allow us to perform complex mathematical calculations.  In this chapter we will introduce a module that allows us to create a data object called a **turtle** that can be used to draw pictures.

You include a module in your program with the line:

    import *module_name*

for example:

    import turtle



Python Turtles
----------------
Turtle graphics, as it is known, is based on a very simple idea. Imagine that you have a turtle that understands English.  You can tell your turtle to do simple commands such as go forward and turn right.  As the turtle moves around, if its tail is down touching the ground, it will draw a line (leaving a trail behind) as it moves.  If you tell your turtle to lift up its tail it can still move around but will not leave a trail.  As you will see, you can make some pretty amazing drawings with this simple capability.

.. note::

    The turtles are fun, but the real purpose of the chapter is to teach ourselves
    a little more Python and to develop our theme of *computational thinking*,
    or *thinking like a computer scientist*.  Most of the Python covered here will
    be explored in more depth later.

.. activecode:: lps-hyt-code1
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



.. index:: turtle, module
|
|
|

:sctnhead:`Glossary and Terms`

import
    A statement used to include a library (or module) in your program. 
    
module
    A python library that adds more functionality to python.
    
turtle
    A python object that can be used for drawing.
        
