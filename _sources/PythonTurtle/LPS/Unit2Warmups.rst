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
   :prefix: lps_u2warm-
   :start: 1



Unit 2 Launches
==================

:sctnhead:`Basic Turtles`

**Exercice 1.**

.. parsonsprob:: lps_u2warm-par1

    The following program uses a turtle to draw a checkmark as shown to the left, <img src="../../_static/TurtleCheckmark4a.png" width="150" align="left" hspace="10" vspace="5" /> but the lines are mixed up.  The program should do all necessary set-up: import the turtle module, get the window to draw on, and create the turtle.  The turtle should turn to face northwest, draw a line that is 75 pixels long, then turn to face southwest, and draw a line that is 150 pixels long.  We have added a compass to the picture to indicate the directions north, south, west, and east.  Northeast is between north and east. Southeast is between south and east. <br /><br /><p>Drag the blocks of statements from the left column to the right column and put them in the right order.  Then click on <i>Check Me</i> to see if you are right. You will be told if any of the lines are in the wrong order.</p>
    -----
    import turtle
    window = turtle.Screen()
    maria = turtle.Turtle()
    maria.left(135)
    maria.forward(75)
    maria.left(90)
    maria.forward(150)

**Exercice 2.**

A pentagon has an internal angle of 108 degrees.  Draw a pentagon with a side of length 75.

.. activecode:: lps_u2warm_code1
    :nocodelens:
    :above:

    import turtle               # allows us to use the turtles library
    wn = turtle.Screen()        # creates a graphics window
    alicia = turtle.Turtle()    # create a turtle named alicia

    ## draw a pentagon.  Remeber to turn 180 - internal angle.
    
   

