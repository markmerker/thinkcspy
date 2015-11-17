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
   :prefix: lps-func2-
   :start: 1



5. Functions (Part 2)
----------------------

Return values
================

Aside from performing tasks, functions also have the ability to return the results of work they perform.  We have already seen some built-in functions that do this.  Below are some of these functions, with an explanation of what they do. 


    abs(num)
        returns the absolute value of ``num``. If ``num`` is an int, returns an int, if ``num`` is a float, returns a float.

    input(prompt)
        display  ``prompt`` to the user, and get what they type in response. Returns a string containing the user's response.
    
    type(item)
        returns a string describing the data type of ``item``.


If a function does return a value, the value can be saved by assigning it to a variable

.. code-block:: python

    x = abs( -20.0)
    abs( -15 )
    
In the above example, x is set to 20.0.  The value 15, returned in the second line, is not used, and hence lost after the line is executed.


::

If a function doesn't return a value, a variable is empty if you set in to the return

         x = drawSquare()
loads x with nothing.  It will still draw the square. 

..

Here is some code that will defines and executes some simple commands.  This code has at least two errors in it.  If we fix the errors, what will be the output of this code?

.. activecode:: lps_func2_sample_1
    :nocodelens:
    :above:

    # DEFINE FUNCTION
    def addAbsolutes( a, b, c ):
        sum = abs( a ) + abs( b ) + abs( c )
        return sum

    x = -14
    y = 12
    z = 2
    sum = a + b + c
    print( "Sum of",x,y, "and", z, "is", sum )
    sum = addAbsolutes( x, y, z )
    print( "Absolute sum of",x, y, "and", z, "is", sum )
    
**Things to notice**

- All code that is part of addAbsolutes is indented.

- The value of the variable ``sum`` changes.  On line 9 ``sum`` is set to 0 and printed on line 10. Then its value is set again on line 11 to the value 28, and printed on line 12.



**Exercise 1. Averages** 

::

Modify this code so the function getAverage() calculates the function for the 4 numbers it is passed, and prints the results.

HINT: Remember to use spaces, not tabs when indenting code.

.. activecode:: lps_func2_code1
    :above:


    # DEFINE FUNCTION
    def getAverage( a, b, c, d ):
        ## calculate the sum of the numbers
        sum = ?????
        ## calculate the average by dividing the sum by 4.0.  
        avg = ?????
        ## return the average
       
  
    ## starting values
    w = 19
    x = 27
    y = 12
    z = 29
    average = getAverage( ???? )
        ## print numbers and their average
    print( "Average of",w, x, y, "and", z, "is", ????? )
    
    ## try  some other values
    y = 99
    z = 50
    average = getAverage( ???? )
        ## print numbers and their average
    print( "Average of",w, x, y, "and", z, "is", ???? )
    

::

Now copy the getAverage() function from exercise 1 to the code for exercise 2.  This time, instead of just setting the numbers, use the input function to prompt the user for the four numbers.  

HINT: When you run your code, it may crash due to a type problem.  Remember the input function returns a string value.

**Exercise 2. Prompt and Average**

Prompt the user for four numbers, then display the numbers and their average.
    
.. activecode:: lps_func2_code2
    :above:


    # DEFINE FUNCTION
    def getAverage( a, b, c, d ):


    ## set values of w, x, y and z
    w = input( "Enter first number" )
    x = input( "Enter 2nd number" )
    y = ???
    z = ???
    
    w = int( w )

    average = getAverage( ???? )
        ## print numbers and their average
    print( "Average of",w, x, y, "and", z, "is", ???? )



**Exercise 3. Back to Triangle One**

Let's revisit drawing a triangle.  In this version, the turtle that does the drawing is a parameter.   The size of the triangle is also a parameter.  

You must write the code that moves the turtle before drawing a triangle.


.. activecode:: lps_func2_code3
    :nocodelens:
    :above:

        #SET UP
    import turtle
    wn = turtle.Screen()
    wn.exitonclick()
    t = turtle.Turtle()


    # DEFINE FUNCTIONS
    def drawTriangle( tur, sz ):
        tur.forward( sz )
        tur.left( 120 )
        tur.forward( sz )
        tur.left( 120 )
        tur.forward( sz )
        tur.left( 120 )

    def moveTurtle( turtl, x , y ):
        pass
        ## Raise pen, move turtle to x,y and lower pen
        

    size = input( "Enter size of triangle" )
    x = input ("Enter x coordinate") 
    y = input ("Enter y coordinate") 

    moveTurtle( t, int(x), int(y) )
    drawTriangle( t, size )



**Exercise 4. A single function**

Copy the function moveTurtle from exercise 3.  Now add a new function.  The goal of this function is to provide a lot features in a single call. 


    drawColoredTriangleAt( turtl, x, y, size, color )
        given a turtle, x-y coordinates, a size and a color, locate the turtle, set its color, then draw a triangle of the requested size.

    Reminder: the function turtle.color( color_name ) sets the turtles color.

.. activecode:: lps_func2_code4
    :nocodelens:
    :above:


    # DEFINE FUNCTIONS
    def drawTriangle( turtl, size ):
        turtl.forward( size )
        turtl.left( 120 )
        turtl.forward( size )
        turtl.left( 120 )
        turtl.forward( size )
        turtl.left( 120 )

    def moveTurtle( turtl, x , y ):
        ??????
        
    def drawColoredTriangleAt( turtl, x, y, size, color ):
        ## set turtles color
        
        ## move the turtle
        
        ## draw the triangle
        

        
        #SET UP
    import turtle
    wn = turtle.Screen()
    wn.exitonclick()
    t = turtle.Turtle()

        ## Get user input
    color = input( "Enter triangle color" )
    x = inputInt( "Enter x coordinate" ) 
    x = int( x )
    y = inputInt( "Enter y coordinate" ) 
    y = int( y )
    size = inputInt( "Enter triangle size" )
    size = int( size )
        
        ## draw the triangle
    
    drawColoredTriangleAt( ??????  )


.. index:: function, parameter, argument, invoke, call 

|
|
|

:sctnhead:`Glossary and Terms`


return value
    Value returned by a function to the code that calls it.





