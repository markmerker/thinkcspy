..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. |NOTE| image:: ../../_static/LPS/pencil.png

.. role:: notetext

.. raw:: html

    <style> .notetext {color:green; font-weight: bold; font-size: 110%; } </style>

.. role:: sctnhead

.. raw:: html

    <style> .sctnhead {color:black; font-weight: bold; font-size: 140%; } </style>
    
.. qnum::
   :prefix: lps_tfl_
   :start: 1


4. The ``for`` Loop
---------------------



When we drew the square, it was tedious.  We had to move then turn, move
then turn, etc. etc. four times.  If we were drawing a hexagon, or an octagon,
or a polygon with 42 sides, it would have been a nightmare to duplicate all that code.

A basic ability of all programs is to repeat some code over and over again. |NOTE| :notetext:`Iteration means repetition of a set of operations.`  In this section, we will explore a basic mechanism for iteration.

The **for** statement allows us to write programs that implement iteration.  It repeats an operation for each item in a sequence.  Your will remember drawing a square involved code like this:

.. sourcecode:: python

    t.forward( 50)
    t.left( 90 )
    t.forward( 50)
    t.left( 90 )
    t.forward( 50)
    t.left( 90 )
    t.forward( 50)
    t.left( 90 )

With a for loop, this is simplified down to

.. sourcecode:: python

    for i in [1,2,3,4] :
        t.left( 90 )
        t.forward( 50)

In python, the list of numbers in the square brackets is called a **list**.  Lists are very useful.  We will have much to say about them later.  

This code sets the variable i to each of the values 1, 2, 3 and 4. For each value of i, it executes the two operation t.forward() and t.left(). Hence, it repeats four times, drawing the square.

Next lesson we will study the syntax of the for loop, and different ways it can be used.  For this lesson, we will just use it for some simple repetition.

Here is the layout of a standard for loop

|    **for** *variable_name*  **in** *list* **:**
|        statement
|        statement
|        ...
 
**There are several important things to know in order to use a ``for loop`` (or ``for statement``).** 

- The first line sets up statement, and ends with a **:**.

- *variable_name* is the variable that will be loaded with each item in the list.  It can be used in the statements.

- *list* is a list of items inside square brackets **[]**.

- The indented statements are called the **loop body**.  There can be one to many statements in the body. **They must all be indented to the same level, or an error will occur.** All the statements are executed each **iteration** or pass through the loop. 

- The next un-indented statement ends the loop's body.


Lets draw some polygons.   

Start with a triangle.  he internal angle of an equilateral triangle is 60 degrees.

.. activecode:: lps_tfl_sample_1
    :nocodelens:
    :above:
    
    
    #SET UP
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t
    side = 100

    ## CALC ANGLE
    intAngle = 60
    turnAngle = 180 - intAngle
    
    # DRAW A TRIANGLE
    for i in [1,2,3]:
        t.left( turnAngle )
        t.forward( side )


The internal angle of a square is 90 degrees.  Finish this code to draw on now

.. activecode:: lps_tfl_sample_1
    :nocodelens:
    :above:
    
    
    #SET UP
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t
    side = 100

    ## CALC ANGLE
    intAngle = 90
    turnAngle = 180 - intAngle
    
    # DRAW A SQUARE
    for i in [1,2,3,4]:



The internal angle of hexagon is 120 degrees.  Draw one now.    


.. activecode:: lps_tfl_sample_1
    :nocodelens:
    :above:
    
    
    #SET UP
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t
    side = 70
    
    ## CALC ANGLE
    intAngle = 
    turnAngle = 
    
    # DRAW THE HEXAGON



The Range Function 
=====================

The formula for the internal angle of for any regular polygon is:

|   **(180 * (sides-2)) / sides )**

Using this formula, we can have a general program for drawing a regular polygon.  But the size of the list we use in the for statemnt must vary, according to the number of sides.  We must generate a list of the correct length.  The **range()** function can to this for us.  We will learn more about range() later.  The simplest version looks like this

|    **range( n )** generates a list **n** items long.

So if we want to repeat something 10 times, we use

|   for i in range( 10 ) :

**Exercise 1.  Polly done gone.**

With this knowledge, lets write a method that draws a polygon with any number of sides.

.. activecode:: lps_tfl_code_1
    :nocodelens:
    :above:
    
    #SET UP
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t
    size = 40
    
    # GET SIDES and CALC ANGLE
    sidesStr = input( "How any sides should we draw?" )
    sides = int( sidesStr )
    intAngle = (180 * (sides-2)) / sides
    turnAngle = 
    
    # DRAW THE SHAPE


**Exercise 2. Stairway to nowhere**

Problem: Create a staircase with steps 30 pixels high.  The stairs raise a total of 180 pixels.  In code, calculate how many steps you need, and then write the loop to draw them.

Use the problem solving approach we talked about in the last lesson.  Break the problem into sections, and add comments to the code to outline the sections.

.. activecode:: lps_tfl_code_1
    :nocodelens:
    :above:
    
    



.. index:: for loop, iteration, 

|
|
|

:sctnhead:`Glossary and Terms`


for loop
    A python statement that iterates through a sequence of items.

Iteration
    The repetition of a set of operations.
    
 




