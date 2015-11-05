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
   :prefix: lps_u2launch-
   :start: 1



Unit 2 Launch - Functions
============================

Use this stair case code for reference

.. code-block:: python

    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t

    # DEFINE FUNCTION
    def drawStepDown():
       size = 20
       t.forward(size)
       t.right(90)
       t.forward(size)
       t.left(90)
    
    ## Draw steps
    drawStepDown()
    drawStepDown()
    drawStepDown()

:sctnhead:`Each of the following pieces of code is supposed to draw 2 squares,but fails to run.  Find and correct the problem with each.  Use the run button, and the python errors to help you find the problem.`


**Launch 1.**

.. activecode:: lps_u2launch_code1
    :nocodelens:
    :above:

    import turtle         
    wn = turtle.Screen()  
    t = turtle.Turtle()   

    def drawSquare():    
       size = 50
       t.foward(size)
       t.left(90)
       t.foward(size)
       t.left(90)
       t.foward(size)
       t.left(90)
       t.foward(size)
       t.left(90)
        
    t.penup()
    t.goto( -100, 0 )
    t.pendown()
    drawSquare()
    
    t.penup()
    t.goto( 0, 0 )
    t.pendown()
    drawSquare()
 
 
**Launch 2.**

.. activecode:: lps_u2launch_code2
    :nocodelens:
    :above:

    import turtle               
    wn = turtle.Screen()        
    t = turtle.Turtle()         

    def drawSquare():
       size = 50
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
        
    t.penup()
    t.goto( -100, 0 )
    t.pendown()
    drawSquare()
    
    t.penup()
    t.goto( 0, 0 )
    t.pendown()
    drawSquare()
    
    
**Launch 3.**


.. activecode:: lps_u2launch_code3
    :nocodelens:
    :above:

    import turtle               
    wn = turtle.Screen()        
    t = turtle.Turtle()         

    def drawSquare():
      size = 50
      t.forward("size")
      t.left(90)
      t.forward("size")
      t.left(90)
      t.forward("size")
      t.left(90)
      t.forward("size")
      t.left(90)
        
    t.penup()
    t.goto( -100, 0 )
    t.pendown()
    drawSquare()
    
    t.penup()
    t.goto( 0, 0 )
    t.pendown()
    drawSquare()
    
**Launch 4.**

.. activecode:: lps_u2launch_code4
    :nocodelens:
    :above:

    import turtle               
    wn = turtle.Screen()        
    t = turtle.Turtle()         

    def drawSquare():
      size = 50
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
      t.forward(size)
      t.left(90)
        
    t.penup()
    t.goto( -100, 0 )
    t.pendown()
    
    t.penup()
    t.goto( 0, 0 )
    t.pendown()
    
        
