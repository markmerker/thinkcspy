..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. |NOTE| image:: Figures/pencil.png

.. role:: notetext

.. raw:: html

    <style> .notetext {color:green; font-weight: bold; font-size: 110%; } </style>

.. role:: sctnhead

.. raw:: html

    <style> .sctnhead {color:black; font-weight: bold; font-size: 140%; } </style>
    
.. qnum::
   :prefix: lps_oftp-
   :start: 1

2. Our First Turtle Program
--------------------------------

Below is a simple program that does some turtle graphics.  The are a few lines of code needed to set things up.  We will go into detail on them later.  For now, we will just use them so we can start drawing.

Exercise 1.

The program as shown will only draw the first two sides of the rectangle.  

.. activecode:: lps_oftp_code1
    :tour_1: "Overall Tour"; 1-6: Example01_Tour01_Line01; 3: Example01_Tour01_Line02; 4: Example01_Tour01_Line03; 5: Example01_Tour01_Line04; 6: Example01_Tour01_Line05;
    :tour_2: "Line by Line Tour"; 1: Example01_Tour02_Line01; 2: Example01_Tour02_Line02; 3: Example01_Tour02_Line03; 4: Example01_Tour02_Line04; 5: Example01_Tour02_Line05; 6: Example01_Tour02_Line06;
    :nocodelens:
    :above:

    import turtle               # allows us to use the turtles library
    wn = turtle.Screen()        # creates a graphics window
    alex = turtle.Turtle()      # create a turtle named alex
    alex.forward(150)           # tell alex to move forward by 150 units
    alex.left(90)               # turn by 90 degrees
    alex.forward(75)            # complete the second side of a rectangle


**Things to notice**

- Line 2 creates the screen the turtle will draw in.

- Line 3 of this program creates a turtle **object**, and loads it into a variable named alex.

- When the alex is created, it is sitting in the center of the screen facing right.

- In lines 4-6, we instruct the turtle **object** alex to move and to turn. We do this by **invoking** or activating alex's functions, or **methods** --- these are the instructions telling alex what to do.

|NOTE| :notetext:`Functions in an object, like turtle, are also called "methods". They are called by using the name of the object followed by a ".".`

|NOTE| :notetext:`To "invoke" is to call a function or method.`

By re-using the commands already in the program, you should be able to draw a complete rectangle.  Try it now above in Exercise 1.

-------------------------------------------------

-------------------------------------------------

The Turtle object provides lots different methods you can use while drawing.  A few are listed below.  

=========== ======= =============== ============== =============================================================================================================   
        Turtle Functions
----------------------------------------------------------------------------------------------------------------------------------------------------------------
Function    Short   Paramters       Examples       Notes 
            name                                   
=========== ======= =============== ============== =============================================================================================================   
forward     fd()    steps           forward(50)    Move forward *steps* pixels.
backward    bk()    steps           backward(18)   Move forward *steps* pixels.
right       rt()    degrees         right(30)      Turn right by the number of *degrees*
left        lt()    degrees         left(30)       Turn left by the number of *degrees*
circle              radius          cicle(25)      Draw a circle with size *radius* 
setheading  seth()  degrees         setheading(45) Point turtle degrees from east (right).0 points right, 45 points toward the top-right, 90 straight up, etc.
pendown     down()                  pendown()      Put pen to paper, e.g. draw when turtle moves.
penup       up()                    penup()        Lift pen from paper, e.g. don't draw when turtle moves.
pensize     width() pixels          pensize(12)    Make pen *pixels* wide.
color               name            color("red")   Set pen color to a name. Some names work, some don't.
color               r,g,b           color(1,5,9)   Set color using values from 0 to 255 for red, green and blue.
=========== ======= =============== ============== =============================================================================================================   


Exercise 2.

Take some time to draw whatever you like in the code box below, using these methods.  Your turtle is names "alicia".  When you have played around some, use the "Save" button to save your first turtle code.

.. activecode:: lps_oftp_code2
    :nocodelens:
    :above:

    import turtle               # allows us to use the turtles library
    wn = turtle.Screen()        # creates a graphics window
    alicia = turtle.Turtle()    # create a turtle named alicia

    ## start drawing !!!
    


.. index:: turtle, method, invoke

|
|
|

:sctnhead:`Glossary and Terms`


method
    A function that is defined and used inside an object, like a turtle.

invoke
    To call a function or method.
    
turtle
    A python object that can be used for drawing.
        
