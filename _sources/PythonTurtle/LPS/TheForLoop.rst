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


6. The ``for`` Loop
---------------------



When we drew the square, it was tedious.  We had to move then turn, move
then turn, etc. etc. four times.  If we were drawing a hexagon, or an octagon,
or a polygon with 42 sides, it would have been a nightmare to duplicate all that code.

A basic ability of all programs is to repeat some code over and over again. |NOTE| :notetext:`Iteration means repetition of a set of operations.`  In this section, we will explore a basic mechanism for iteration.

The **for** statement allows us to write programs that implement iteration.  It repeats an operation for each item in a sequence.  Your will remember drawing a square involved code like this:

.. sourcecode:: python

    # drawing a square
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

    # drawing a square
    for i in [1,2,3,4] :
        t.left( 90 )
        t.forward( 50)

In python, the sequence of numbers in the square brackets is called a **list**.  Lists are very useful.  We will have much to say about them later.  

This code sets the variable i to each of the values 1, 2, 3 and 4. For each value of i, it executes the two indented lines of code, the operations t.forward() and t.left(). Hence, it repeats four times, drawing the square.

Lets look at another example


.. activecode:: lps_tfl_sample_1
    :above:
    
    x = 0
    for counter in [ 1, 2, 3, 4 ]:
        print ("Count is ", counter )
        print ("Count squared is ", counter ** 2 ) 
        x = x + counter
        
    print ("x is ", x )
    

**Things to notice**

- Each time the loop executes, ``counter`` has a different value. The value is taken from the list in the first line.

- Since ``counter`` is set to int values, it can be used in expressions like ``x + counter``.

- The variable ``x`` is defined before the loop, and updated within the loop.

- All code that is part of the loop is indented.  This is called the **body**.



**Exercise 1. Being Square**

Your Task

- Modify the code in draw square so that it uses a for loop instead of repeating the same command over and over.


.. activecode:: lps_tfl_code_1
    :above:
    
    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t

    # DEFINE FUNCTION
    def drawSquare( tur ):
       size = 100
       #### change this code to use a for loop
       tur.forward(size)
       tur.left(90)
       tur.forward(size)
       tur.left(90)
       tur.forward(size)
       tur.left(90)
       tur.forward(size)
       tur.left(90)


    drawSquare( t )


**Exercise 2. Three Squares**

Your Tasks

- Write the code for drawSquare using a for loop instead of repeating the same command over and over.

- Fill in the body of the loop ``for x in [ -190, -70, 50 ]`` so that for each value of ``x`` it draws a square at (x,y).

.. activecode:: lps_tfl_code_2
    :above:
    
    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    


    def moveTurtle( turtl, x , y ):
        turtl.penup()
        turtl.goto( x,y)
        turtl.pendown()

    def drawSquare( tur, size):
        #### write a for loop that draws a square



    sz = 100
    y = 0
    for x in [ -190, -70, 50 ]:
        #### move the turtle to x,y
        
        #### draw a square of size sz
        

.. index:: for loop, iteration, list, body  


|
|
|

:sctnhead:`Glossary and Terms`

Body
    The indented section of the loop, which is executed repeatedly.

for loop
    A python statement that iterates through a sequence of items.

Iteration
    The repetition of a set of operations.
    
 
List
    A python data type that hold a sequence of items.  Each item is a value.



