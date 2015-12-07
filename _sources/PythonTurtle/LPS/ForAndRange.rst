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
   :prefix: lps_far_
   :start: 1


7. ``for`` and ``range``
-------------------------

In the previous lesson, we learned that the for statement sets a varaible to each item in a list, and then executes the statement body for each value of the variable.

This when this code exe
cutes:
.. sourcecode:: python
    
   for i in [1,2,3,4] :
      print ( i."squared is ", i * i )

 The actual steps executed by python are:

.. sourcecode:: python

    i = 1
    print ( i."squared is ", i * i )
    i = 2
    print ( i."squared is ", i * i )
    i = 3
    print ( i."squared is ", i * i )
    i = 4
    print ( i."squared is ", i * i )
    

The  Range Function
====================
What if you wanted to repeat something a hundred, or even a thousand times.  Python provides the range.  There are several ways to use it, but the simplest is just to give a single integer, and it creates a list with that many entries.  

.. activecode:: lps_far_sample_1
    :above:
    
    numbers = range( 6 )
    print ("numbers is ", numbers )
    
''The list starts at 0, and goes to one less then the requesed number, but the important thing'' |NOTE| :notetext:`calling range(n) creates a list that is n numbers long.`


So instead of saying:
    

.. sourcecode:: python

    def drawSquare( tur, sz ):
        angle = 90
        for i in [1,2,3,4]:
            tur.forward(sz)
            tur.turn( angle )

we can use

.. sourcecode:: python

    def drawSquare( tur, sz ):
        angle = 90
        for i in range(4):
            tur.forward(sz)
            tur.turn( 180 - angle )

Exercises
==========

**Exercise 1. Drawing polygons using range**

In this exercise, you will be adding and calling functions to draw a pentagon, a hexagon, and an octagon. For all these, use the range function to control number of sides to draw.

The comments with two hashes ``##`` will guide you where you are suposed to enter code.

Here are the internal angles of different polygons:

================ ======= =============== 
   Shape         Sides   Internal angle
================ ======= ===============  
   triangle      3       60
   square        4       90
   pentagon      5       108
   hexagon       6       120
   septagon      7       128.14
   octagon       8       135
   dodecagon     12      150
   Icositetragon 24      165
================ ======= ===============  

Your Task

- Modify the code in drawSquare so that it uses the range fuction
- Modify the drawPentagon code using the range function, and the correct internal angle
- Fill in the missing code in drawHexagon.
- Add the drawOctagon function.

Once you implement a function, remove the # (comment sign) from the call to that function.  Test to make sure it draws properly.

**Extra Credit** Draw some other polygons.

.. activecode:: lps_far_code_1
    :above:
    
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t
    t.speed(30)
    
    def moveTurtle( turtl, x , y ):
        turtl.penup()
        turtl.goto( x,y)
        turtl.pendown()

    def drawSquare( tur, size ):
       internalAngle = 90
       ## fill in range function 
       for i in :
         tur.forward(size)
         tur.left(180 - internalAngle )

    def drawPentgon( tur, size ):
        ## set correct internal angle
       internalAngle = 0
       ## fill in range function 
       for i in []:
         tur.forward(size)
         tur.left(180 - internalAngle )

    def drawHexagon( tur, size ):
        ## set correct internal angle
       internalAngle = 0
        ## finish for statement first line
       for i in []:
         ## fill in for loop body
         pass



    size = 100
    moveTurtle( t, -100, -100 )
    drawSquare( t, size )
    #drawPentgon( t, size )
    #drawHexagon( t, size )
    #drawOctagon( t, size )
    

**Exercise 2. Any Polygon**

Now we write a general function the will draw an  reuar polygon.  To do this, we use a formula the calculate the internal angle, given any number of sides.

    internal angle = (180 * (sides-2)) / sides
    
We have prodived this function in the code, so your code only has to call it.

Your Task

- Fill in the code for drawPolygon.

- Test your code by setting different valuess for the variables sideCount and sideSize.

.. activecode:: lps_far_code_2
    :above:
    
    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    
    t.speed(30)

    def moveTurtle( turtl, x , y ):
        turtl.penup()
        turtl.goto( x,y)
        turtl.pendown()

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)


    def drawPolygon( tur, sides, size):
        #### get internal angle
        internalAngle = 
        
        ### finish header of for loop
        for        :
            ## draw a side of the polygon.

    sideCount = 4
    sideSize = 100
    moveTurtle( t, -100, -100 )
    pen.pensize( 3 )
    pen.color( "blue" )
    drawPolygon( t, sideCount, sideSize )


        

.. index:: for loop, range, list, body  


|
|
|

:sctnhead:`Glossary and Terms`

Body
    The indented section of the loop, which is executed repeatedly.

for loop header
    The first line of the for loop, in which the varaible and list are stated.

range
    A function that returns a list.
    
 
List
    A python data type that hold a sequence of items.  Each item is a value.



