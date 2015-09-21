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
   :prefix: lps-sae-
   :start: 1



Statements and Expressions
-----------------------------------------
    



|NOTE| :notetext:`A statement is an instruction that the Python interpreter can execute.`  It is a command: **do ** *something*. We have only seen two kinds of statements so far. ``Assignment`` statements have = signs, and are used to set the value of a variable. ``Print`` statements output strings to the monitor. Some other kinds of statements that we'll see shortly are ``while``, ``for``, ``if``,  and ``import`` statements.  (There are lots of more as well.)



|NOTE| :notetext:`An expression is a combination of values, variables, operators, and calls to functions that will be evaluated by Python.`

|NOTE| :notetext:`Evaluation is the process of resolving an expression to its final value.`  Evaluating the expression ``1 + 2 + 3 + 4`` yields the value ``10``.

:sctnhead:`Statements vs. Expressions`

While expressions may require python to do work to resolve them, they don't cause python to really take an action.  That is what statements do.  An expression may resolve to `10`, but it doesn't say what to do with that value.  Imagine you have a robot.  If you tell it "Take 2+3 steps forward" it will add the numbers and then take the five steps.  If you tell it "2+3", it may add the numbers to get 5, but it does nothing with the five, because there is a no command to do anything.  "2+3" is an ``expression``, "Take ### steps" forward is a ``statement``.


________________________________________________

Whenever python encounters as expression, it evaluates it, and uses the value in accordance with the statement the expression is found in.  If you ask Python to ``print`` an expression, the interpreter evaluates the expression and displays the result.

.. activecode:: lps-sae-code-1
    :nocanvas:
    :nocodelens:

    print( 1 + 1 )
    print( "hello" )
    print(len("hello"))

**Things to notice**


- The first print statement encounters the expression ``1 + 1`` and evaluates it to the value ``2``. It then takes that value, 2, and prints it to the screen.

- In the second statement, the expression is ``"hello"``, which doesn't really need evaluation, since it is already it's own final value.  It is printed as is.

- In the third statement, the expression is ``len("hello")``.  This expression is actually a call to a python function named ``len`` that returns the length of something.  In this case, it returns the length of the string "hello", which is 5.  Thus 5 is the result of evaluating the expression ``len( "hello" )``, and that result is printed to the screen.

We will learn more about functions soon.  You may notice that this 'len' is the not the first function we have encountered.  We have already seen the functions ``print``, ``type``, ``str``, ``float`` and ``int``.  Each of these functions performs a particular well-defined job.

Evaluation always yields a final value.  All values must be of some data type.  There are many data types, but so far, we have only used 3: ``str``, ``chr`` and ``float``.

|

**Something to think about...**

    Last lesson, were talked about the fact that there is both a function and a data type called  ``str``.  How do we know which is which?  When you see the word ``str`` by itself, it is generally describing a data type.  When you use the function ``str`` it is always followed by parens ``str( ... )``.  The parens surround the data to be passed to the function.  The function ``str`` takes whatever was passed in, and returns a version of that data that is of the string (str) data type.
    And 



.. index:: statement, expression, function

|
|
|

:sctnhead:`Glossary and Terms`


Evaluation
    The processes of converting an expression into a final value.

Expression
    A combination of values, variables, operators, and functions that can be reduced down to a single value.

Function
    Some weird thing thats uses parenthesis.
    
Statement
    An instruction that the Python interpreter can execute.