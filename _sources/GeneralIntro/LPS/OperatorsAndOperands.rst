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
   :prefix: lps-oao-
   :start: 1


Operators and Operands: Part 1
----------------------------------------

**Operators** are special tokens that represent computations, "+" represents addition,
"-" represents subtraction, etc.

The values the operator works on are called
**operands**.  

In the expression ``1 + 2``  the operator is ``+`` and the operands are ``1``, and ``2``.

The following are all legal Python **expressions** whose meaning is more or less
clear::

    20 + 32
    hour - 1
    hour * 60 + minute
    minute / 60
    5 ** 2
    (5 + 9) * (15 - 7)

The operands ``+``, ``-``, and ``*`` mean in Python what they mean in mathematics. The asterisk (``*``), *not x*, is the token for multiplication, and ``**`` is the token for exponents.  ``5 ** 2`` is the same as "5 to the power of 2",  or "5 squared".


Addition, subtraction, multiplication, and exponentiation all do what you expect.  Take a moment and write down what you think the code below will output to the screen.

.. activecode:: lps-oao-code-1
    :nocanvas:
    :nocodelens:

    print(2 + 3)
    print(2 - 3)
    print(2 * 3)
    print(2 ** 3)
    print(3 ** 2)

:sctnhead:`Three Kinds of Division`

Division with computers is a little more interesting than it is in simple arithmetic.  There are actually 3 kinds of division, represented by the symbols  /,  //  and %.   

This exercise has two purposes.  This first is to learn about the three kinds of division.  The second is to learn a little about problem solving.  

Here is the problem:  **What do  /, // and % do?  How are they different?**

Exercise 1.  Step 1.

    Get in code pairs.  For five minutes experiment with different numbers, using the code below.  You can extend the code (add new lines), and/or change it as you like.  After 5 minutes we will stop.  Your pair will report to the class what you did, and what you noticed.  *You probably won't find the answer.  We are as interested in what kind of experiments you did, as in your final results.*

.. activecode:: lps-oao-code-3
    :nocodelens:

    a = 5
    b = 2
    print( a / b )
    print( a // b )
    print( a % b )

..
Exercise 1.  Step 2.
    
    During your experimenting, you may have collected a lot of data, and found it hard to keep track of.  Below is a change to the code, that will make sure all the data is generated every time you run the program, and that it is easy to keep track of.  Once you have this code working, keep experimenting.
    
.. activecode:: lps-oao-code-4
    :nocodelens:
    :hidecode:

    a = 5
    b = 2
    print( "a=",a,"b=", b, "  / result=", a / b , "  // result=", a // b , "  % result=", a % b )
    a = 2
    b = 5
    print( "a=",a,"b=", b, "  / result=", a / b , "  // result=", a // b , "  % result=", a % b )
    ##  keep adding more versions with different a and b values.
    

Exercise 1.  Step 3.
    Still haven't figured out how the different types of division work?  Hidden below is a suggestion that might help.
    
.. reveal:: lps-oao-rev2
    :showtitle:"Show_Suggestion"
    :hidetitle:"Hide_Suggestion"
    
    In order to solve the problem, try to be systematic.  Order your tests in a way that will help you understand what's going on.  For example, set ``a = 7``.  Then execute the problem for every value of b from 1 to 10.  Look for a pattern in the results. Try again with ``a = 3``.

    
    
.. index:: operator, operand, problem solving

|
|
|

:sctnhead:`Glossary and Terms`

Operator
    The symbol ( +, -, *, **, etc.) in an expression that tells what do the numbers.

Operand
    The number(s) in an expression that the operation requested by the operand is performed on. 
