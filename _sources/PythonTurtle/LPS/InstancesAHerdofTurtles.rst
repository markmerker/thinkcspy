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
   :prefix: lps_ihot-
   :start: 1



4. Instances --- A Herd of Turtles
-------------------------------------

We have seen that different variables can hold different values of the same type.

.. sourcecode:: python

    a = 1
    b = 2
    c = a + b
    
In the same way, different variables can hold different versions **(or instances)** of the Turtle class.  Each instance is a turtle with its own data or **attributes** such as location, pen width, color, etc.  Each instance moves on its own, unaffected by the other turtles. The data for each instance is  

|NOTE| :notetext:`instance - an individual version of an object` like a turtle. 

|NOTE| :notetext:`attribute - the data inside an object or instance.`



In this example alex is set to have thin black pen, while tess  has a fat pink one.  Each travels their own path, alex a square, tess a triangle.

.. activecode:: lps_ihot-code1
   :tour_1: "Overall Tour"; 1-31: Example03_Tour01_Line01; 1-3: Example03_Tour01_Line02; 6-8: Example03_Tour01_Line03; 10: Example03_Tour01_Line04; 6,10: Example03_Tour01_Line05; 12-17: Example03_Tour01_Line06; 19-20: Example03_Tour01_Line07; 22-29: Example03_Tour01_Line08; 31: Example03_Tour01_Line09;
   :tour_2: "Line by Line Tour"; 1: Example01_Tour02_Line01; 2: Example01_Tour02_Line02; 3: Example02_Tour02_Line03; 6: Example02_Tour02_Line04; 7: Example03_Tour02_Line05; 8: Example03_Tour02_Line06; 10: Example01_Tour02_Line03; 6,10: Example03_Tour01_Line05; 12-17: Example03_Tour02_Line09; 12-13: Example03_Tour02_Line10; 12: Example03_Tour02_Line11; 13: Example03_Tour02_Line12; 14-15: Example03_Tour02_Line13; 14: Example03_Tour02_Line14; 15: Example03_Tour02_Line15; 16-17: Example03_Tour02_Line16; 16: Example03_Tour02_Line17; 17: Example03_Tour02_Line18; 19-20: Example03_Tour01_Line07; 19: Example03_Tour02_Line20; 20: Example03_Tour02_Line21; 22-29: Example03_Tour01_Line08; 10: Example03_Tour02_Line23; 22-23: Example03_Tour02_Line24; 22: Example03_Tour02_Line25; 23: Example03_Tour02_Line26; 24-25: Example03_Tour02_Line27; 26-27: Example03_Tour02_Line28; 28-29: Example03_Tour02_Line29; 31: Example02_Tour02_Line10;
   :nocodelens:
   
   import turtle
   wn = turtle.Screen()             # Set up the window and its attributes
   wn.bgcolor("lightgreen")


   tess = turtle.Turtle()           # create tess and set some attributes
   tess.color("hotpink")
   tess.pensize(5)

   alex = turtle.Turtle()           # create alex

   tess.forward(80)                 # Let tess draw an equilateral triangle
   tess.left(120)
   tess.forward(80)
   tess.left(120)
   tess.forward(80)
   tess.left(120)                   # complete the triangle
        ## turn tess around, and move off of
        ##  the origin without drawing.
   tess.penup()
   tess.right(180)                  
   tess.forward(80)   

   alex.forward(50)                 # make alex draw a square
   alex.left(90)
   alex.forward(50)
   alex.left(90)
   alex.forward(50)
   alex.left(90)
   alex.forward(50)
   alex.left(90)

   wn.exitonclick()


**Things to notice**

* There are 360 degrees in a full circle.  If you add up all the turns that a
  turtle makes, *no matter what steps occurred between the turns*, you can
  easily figure out if they add up to some multiple of 360.  This should
  convince you that alex is facing in exactly the same direction as he was when
  he was first created. (Geometry conventions have 0 degrees facing East and
  that is the case here too!)
* We could have left out the last turn for alex, but it is a good habit for him to be facing the same way he was at the start. That way the next piece of code can better know what to expect.
* Tess also makes a turn to her original position at the end of the triangle.


**Check your understanding**

.. mchoice:: test_question3_2_1
   :answer_a: True
   :answer_b: False
   :correct: b
   :feedback_a: You can create and use as many turtles as you like.  As long as they have different names, you can operate them independently, and make them move in any order you like.  To convince yourself this is true, try interleaving the instructions for alex and tess in ActiveCode box 3.
   :feedback_b: You can create and use as many turtles as you like.  As long as they have different names, you can operate them independently, and make them move in any order you like.  If you are not totally convinced, try interleaving the instructions for alex and tess in ActiveCode box 3.

   True or False: You can only have one active turtle at a time.  If you create a second one, you will no longer be able to access or use the first.

**Mixed up programs**

.. parsonsprob:: 3_6

   The following program has one turtle, "jamal", draw a capital L in blue and then another, "tina", draw a line to the west in orange as shown to the left, <img src="../_static/TwoTurtles1.png" width="150" align="left" hspace="10" vspace="5" />.  The program should do all set-up, have "jamal" draw the L, and then have "tina" draw the line.   Finally, it should set the window to close when the user clicks in it.<br /><br /><p>Drag the blocks of statements from the left column to the right column and put them in the right order.  Then click on <i>Check Me</i> to see if you are right. You will be told if any of the lines are in the wrong order.</p>
   -----
   import turtle
   wn = turtle.Screen()
   =====        
   jamal = turtle.Turtle()
   jamal.pensize(10)
   jamal.color("blue")                                 
   jamal.right(90)
   jamal.forward(150)
   ===== 
   jamal.left(90)
   jamal.forward(75)
   =====
   tina = turtle.Turtle()
   tina.pensize(10)
   tina.color("orange")
   tina.left(180)
   tina.forward(75)
   =====
   wn.exitonclick()

.. parsonsprob:: 3_7

   The following program has one turtle, "jamal", draw a line to the north in blue and then another, "tina", draw a line to the east in orange as shown to the left, <img src="../_static/TwoTurtlesL.png" width="150" align="left" hspace="10" vspace="5" />.  The program should import the turtle module, get the window to draw on, create the turtle "jamal", have it draw a line to the north, then create the turtle "tina", and have it draw a line to the east.  Finally, it should set the window to close when the user clicks in it.<br /><br /><p>Drag the blocks of statements from the left column to the right column and put them in the right order.  Then click on <i>Check Me</i> to see if you are right. You will be told if any of the lines are in the wrong order.</p> 
   -----
   import turtle
   =====
   wn = turtle.Screen()
   =====    
   jamal = turtle.Turtle()
   jamal.color("blue") 
   jamal.pensize(10)   
   =====                               
   jamal.left(90)
   jamal.forward(150)
   =====
   tina = turtle.Turtle()
   tina.pensize(10)  
   tina.color("orange")
   tina.forward(150)
   =====
   wn.exitonclick()


Regular Polygons
==================

::

There is a formula for the internal angle of a polygon. It is:
    
    (180 * (number of sides - 2 ) / (number of sides)
    
for example a rectangle's internal angle is
     (180 * (4 - 2) ) / 4 = (180 * 2) / 4 = 90
a triangle
     (180 * (3 - 2) ) / 3 = (180) / 3 = 60

When drawing polygons with turtles, you don't turn the value of the internal angle, but 180 minus that angle.  So to draw a triangle, we turn not 60 degrees, but 180 minus 60, or 120 degrees.


**Exercise 1.**

Using 3 different turtles draw a hexagon, septagon and octagon.

.. activecode:: lps_ihot-code1
    :nocodelens:
    :above:

    import turtle 
    wn = turtle.Screen()
    hex = turtle.Turtle()
    hex.color("red")
    hex.pensize( 2 )
    
    sept = turtle.Turtle()
    sept.color("darkblue")
    sept.pensize( 3 )
    
    oct = turtle.Turtle()
    oct.color("green")
    oct.pensize( 4 )
    
    ## calculate the internal angle for a hexagon
    
    ## use the angle, and draw 6 lines and angles using hex
    
    
    ## calculate the internal angle for a septagon
    
    ## use the angle, and 7 draw lines and angles using sept
    
    
    ## calculate the internal angle for an octagon
    
    ## use the angle, and 8 draw lines and angles using oct.
    
    
    
.. index:: turtle, method, invoke

|
|
|

:sctnhead:`Glossary and Terms`


attribute
    Data contained within an object.
    
instance
    A single version of an object.

