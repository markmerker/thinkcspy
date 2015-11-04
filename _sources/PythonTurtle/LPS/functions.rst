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
   :prefix: lps-func-
   :start: 1



Functions
---------


In Python, a **function** is a named sequence of statements
that belong together. Most programming involves creating and using functions. Their primary purpose is to help us
organize programs into chunks that match how we think about
the solution to the problem.

To use a function, we must do two things:

1 We must define (or declare) it.  The definition does not run immediately.  It only tells the python what to do if the function is called.

2 We must call (or invoke) the function.


Defining a Function
=====================
The **function definition** tells Python the name of the function, and exactly what it does.  It does not actually run the function.  The syntax is

.. code-block:: python

    def name( parameter, parameter, ... ):
        body

**On the first line**

``def`` is a reserved Python word that means we are defining a function.

``name`` is any name you want to give the function (that's a legal name, and not a keyword).

After ``name`` are parenthesis, which can contain zero to many parameters.  

The parens  ``must be followed by a colon`` **:**

The **body** is a list of one or more statements.  They all have to be indented from the ``def`` by the same amount. In the examples in this book, we will use the standard indentation of four spaces. These will be executed when the function is called. 

Here's an example

.. code-block:: python

    def drawStepDown():
        size = 20
        t.forward(size)
        t.right(90)
        t.forward(size)
        t.left(90)


Calling a Function
=====================

The code inside the function is only run when the function is called (or invoked.)  This is done by using the function name, followed by parenthesis.
       
.. code-block:: python

    x = 1
    drawStepDown()
    y = 2


After the line ``x= 1`` is run, the function ``drawStepDown()`` is called and run.  When it is done, the program returns to where is was, and executes the next line, ``y = 2``.



Here is some code that will draw a stairway with 5 steps.

.. activecode:: lps_func_sample_1
    :nocodelens:
    :above:

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

    ## locate turtle
    t.penup()
    t.goto( -100, 100 )
    t.pendown()
    
    ## Draw steps
    drawStepDown()
    drawStepDown()
    drawStepDown()
    drawStepDown()
    drawStepDown()

**Exercise 1. Going up** 

Write code that defines a function drawStepUp().  Then draw a stairway that goes up 5 steps.

.. activecode:: lps_func_code1
    :nocodelens:
    :above:

    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t

    # DEFINE FUNCTION
    def drawStepUp():
       size = 20
       ## turn turtle to point up
       
       ## move up
       
       ## point turtle to the right
       
       ## move right
       
       

    ## locate turtle
    t.penup()
    t.goto( ???, ??? )
    t.pendown()
    
    ## Draw steps

    
Let's revisit a problems from the lab.

**Exercise 2. Three Squares**

Draw three squares, next to each other.  Make each side 100.  The squares shouldn't touch.

.. image:: Figures/u2_3_squares.png

    
.. activecode:: lps_func_code2
    :nocodelens:
    :above:

    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    # create a turtle named t

    # DEFINE FUNCTION
    def drawSquare():
       size = 100
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)


    ## FIRST SQUARE
        ## locate turtle
    t.penup()
    t.goto( -190,0  )
    t.pendown()
    
        ## draw the square

    ## SECOND  SQUARE
        ## locate turtle
    
        ## draw the square
    
    ## THIRD SQUARE
        ## locate turtle
    
        ## draw the square

**Exercise 3. Three Triangles**

Draw three triangles, next to each other.  They shouldn't touch.  Use a function for drawing the triangle.  

Hint: to draw a triangle the turtle must make 120 degree turns.

    
.. activecode:: lps_func_code3
    :nocodelens:
    :above:

    # SET UP 
    import turtle           
    wn = turtle.Screen()    
    t = turtle.Turtle()    

    ## define function drawTriangle
    

    ## locate turtle
    
    ## draw first triangle

    ## locate turtle
    
    ## draw second triangle

    ## locate turtle
    
    ## draw third triangle
    

Parameters 
=============

Functions are much more useful when they take ``parameters`` or arguments. A function definition can have a list of parameters.  Each is a variable name.  When the function is called, it is called with a list of values, the same length as the list of parameters.  The values in the function call are loaded into the corresponding variables.


Here is an example.

.. code-block:: python


    def drawSquare( size ):
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)
       t.forward(size)
       t.left(90)

Later in the code, we call:

.. code-block:: python

    drawSquare( 120 )
    
Since 120 is passed the parameter, ``drawSquare`` sets the value of ``size`` to 120, and then executes the code. A square of size 120 is drawn.


Here is an example with 2 parameters:

    def moveWithoutDrawing( x , y ):
        t.penup()
        t.goto( x, y )
        t.pendown()

Later in the code, we call:

.. code-block:: python

    moveWithoutDrawing( 50, 10 )

In this example. when called ``moveWithoutDrawing`` sets the ``x`` to 50 and ``y`` to 10.The pen is lifted, the turtle moves to (50,10), and the pen is lowered.
    




**Check your understanding**

.. mchoice:: test_question5_1_1
   :answer_a: A named sequence of statements.
   :answer_b: Any sequence of statements.
   :answer_c: A mathematical expression that calculates a value.
   :answer_d: A statement of the form x = 5 + 4.
   :correct: a
   :feedback_a: Yes, a function is a named sequence of statements.
   :feedback_b: While functions contain sequences of statements, not all sequences of statements are considered functions.
   :feedback_c: While some functions do calculate values, the python idea of a function is slightly different from the mathematical idea of a function in that not all functions calculate values.  Consider, for example, the turtle functions in this section.   They made the turtle draw a specific shape, rather than calculating a value.
   :feedback_d: This statement is called an assignment statement.  It assigns the value on the right (9), to the name on the left (x).

   What is a function in Python?

.. mchoice:: test_question5_1_2
   :answer_a: To improve the speed of execution
   :answer_b: To help the programmer organize programs into chunks that match how they think about the solution to the problem.
   :answer_c: All Python programs must be written using functions
   :answer_d: To calculate values.
   :correct: b
   :feedback_a: Functions have little effect on how fast the program runs.
   :feedback_b: While functions are not required, they help the programmer better think about the solution by organizing pieces of the solution into logical chunks that can be reused.
   :feedback_c: In the first several chapters, you have seen many examples of Python programs written without the use of functions.  While writing and using functions is desirable and essential for good programming style as your programs get longer, it is not required.
   :feedback_d: Not all functions calculate values.

   What is one main purpose of a function?

.. mchoice:: test_question5_1_3
   :answer_a: def drawCircle(t):
   :answer_b: def drawCircle:
   :answer_c: drawCircle(t, sz):
   :answer_d: def drawCircle(t, sz)
   :correct: a
   :feedback_a: A function may take zero or more parameters.  It does not have to have two.  In this case the size of the circle might be specified in the body of the function.
   :feedback_b: A function needs to specify its parameters in its header.
   :feedback_c: A function definition needs to include the keyword def.
   :feedback_d: A function definition header must end in a colon (:).

   Which of the following is a valid function header (first line of a function definition)?

.. mchoice:: test_question5_1_4
   :answer_a: def drawSquare(t, sz)
   :answer_b: drawSquare
   :answer_c: drawSquare(t, sz)
   :answer_d: Make turtle t draw a square with side sz.
   :correct: b
   :feedback_a: This line is the complete function header (except for the semi-colon) which includes the name as well as several other components.
   :feedback_b: Yes, the name of the function is given after the keyword def and before the list of parameters.
   :feedback_c: This includes the function name and its parameters
   :feedback_d: This is a comment stating what the function does.

   What is the name of the following function?

   .. code-block:: python

     def drawSquare(t, sz):
         """Make turtle t draw a square of with side sz."""
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)



.. mchoice:: test_question5_1_5
   :answer_a: i
   :answer_b: t
   :answer_c: t, sz
   :answer_d: t, sz, i
   :correct: c
   :feedback_a: i is a variable used inside of the function, but not a parameter, which is passed in to the function.
   :feedback_b: t is only one of the parameters to this function.
   :feedback_c: Yes, the function specifies two parameters: t and sz.
   :feedback_d: the parameters include only those variables whose values that the function expects to receive as input.  They are specified in the header of the function.

   What are the parameters of the following function?

   .. code-block:: python

     def drawSquare(t, sz):
         """Make turtle t draw a square of with side sz."""
         for i in range(4):
             t.forward(sz)
             t.left(90)



.. mchoice:: test_question5_1_6
   :answer_a: def drawSquare(t, sz)
   :answer_b: drawSquare
   :answer_c: drawSquare(10)
   :answer_d: drawSquare(alex, 10):
   :answer_e: drawSquare(alex, 10)
   :correct: e
   :feedback_a: No, t and sz are the names of the formal parameters to this function.  When the function is called, it requires actual values to be passed in.
   :feedback_b: A function call always requires parentheses after the name of the function.
   :feedback_c: This function takes two parameters (arguments)
   :feedback_d: A colon is only required in a function definition.  It will cause an error with a function call.
   :feedback_e: Since alex was already previously defined and 10 is a value, we have passed in two correct values for this function.

   Considering the function below, which of the following statements correctly invokes, or calls, this function (i.e., causes it to run)?  Assume we already have a turtle named alex.

   .. code-block:: python

     def drawSquare(t, sz):
         """Make turtle t draw a square of with side sz."""
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)
         t.forward(sz)
         t.left(90)


.. index:: function, parameter, argument, invoke, call 

|
|
|

:sctnhead:`Glossary and Terms`


argument
    The same thing as a parameter.

call
    To tell python to run a function.
    
   
function
    A named set of statements, used to organize code into manageable pieces.
    

invoke
    the same thing as call.
    
    
parameter
    A value that is passed into a function.  the value can vary each time the function is called.




