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
   :prefix: lps-oao2-
   :start: 1


Operators and Operands: Part 2
----------------------------------------

:sctnhead:`The Three Faces of Division`

We figured out in the last lesson the three different kinds of arithmetic.  Each has a different operand to invoke it.

    Division ``\``
        Good old decimal (floating point) division.  Results are **always a float**, even if the operands are both ints.
    
    Integer Division ``\\``
        The result is always an integer (whole number), and **always rounded down**.  Thus ``100 // 99 `` is ``9``, even though the decimal answer is ``9.9``, and if we were rounding it would be ``10``.  Cutting off the decimal part of the number is sometimes called **truncating**.
    
    Modular Division  ``%``
        Called 'remainder division', or more often, just 'mod'.  The result is the remainder from integer division. When speaking code we say  *"4 mod 3"*.  Examples:     ``4 % 3  is 1`` ,  ``100 % 9 is 1`` , ``5 % 5 is 0`` , ``422 % 211 is 0`` , ``423 % 211 is 1``
        

:sctnhead:`Variables and Data Types in Expressions`

When a variable name appears in the place of an operand, it is replaced with
the value that it refers to before the operation is performed.
For example, here we convert 645 minutes into hours.  


This code shows the use of variables as operands.  The code tried to solve the problem: Think about the problem, 645 minutes is how many hours? 

.. activecode:: lps-oao2-code1
    :nocanvas:
    :nocodelens:
    :hidecode:
    
    total_minutes = 645
    hours = total_minutes / 60
    print( total_minutes, "minutes is", hours, "hours" )
    

This example also shows us how useful integer division and modular division are.

.. activecode:: lps-oao2-code2
    :nocanvas:
    :nocodelens:
    
    total_minutes = 645
    hours = total_minutes // 60
    minutes = total_minutes % 60
    print( total_minutes, "minutes is", hours, "hours and", minutes, "minutes" )
    


In python, it is legal to perform operations that use both integers and floats.  Whenever you use both together, the result is always a float.  If you use decimal division (/), the result is always a float.

It is legal to use strings with the **+** operator, but not with any others.

It is not legal to perform an operation using numbers and strings together (unless you first convert the data type of one or the other.)

::
    
    20 + 32             ## legal
    hour = 1  
    minute = 60.0
    hour * 60 + minute  ## legal
    99 + 8.32           ## legal
    "99" + 4            ## ILLEGAL
    int( 99 ) + 4       ## legal
    "hi" + " mom"       ## legal
    "99" + str(4)       ## legal
    "99" - str(4)       ## ILLEGAL
    hi = "hi"
    mom = 12
    hi + mom            ## ILLEGAL
    
Exercise 1.
    Fill in the expected results of the expressions on the activity sheet.  Then test your results by entering them into the python window below.  If thee expression is illegal, python will generate an error. 


.. activecode:: lps-oao2-code3
    :nocanvas:
    :nocodelens:

    print( 20 + 32 )

:sctnhead:`Let's Write Some Code`

Although we are still at the very begriming, we know enough to write some simple code. The first exercise is described, and then answered.  After that, you are on your own.  Be sure to save all your results, so they get submitted to the teachers.

Exercise 2.
    Find the average of the numbers  ``27.1, 18.5, 0 and 19``.  When you write the code, follow these steps:
    
    - Calculate the total, saving it in a variable named "total"
    - Calculate the average,  saving it in a variable named "average"
    - Print your answer so it appears on the screen like this:  "The average is *????*"
    
Answer 1.

.. activecode:: lps-oao2-code4
    :nocanvas:
    :nocodelens:
    :above:

    total = 27.1 + 18.5 + 0 + 19
    average = total / 4
    print( "The average is", average )

Exercise 3.
    How many minutes and seconds are there in 987 seconds?
    
    - set the variable "total_time" to 987.
    - Calculate the integer number of minutes, saving it in a variable named "minutes"
    - Calculate the number of seconds left over from the first calculation.Save it in a variable named "seconds"
    - Print your answer so it appears on the screen like this  
            "987 seconds is *????* minutes and *????* seconds."
    
.. activecode:: lps-oao2-code5
    :nocanvas:
    :nocodelens:
    :above:

    total_time = 987


Exercise 4.
    You have a box that's 18 inches high, 12 inches wide, and 12 inches long.  How many cubic inches can it hold? This quantity is the volume of the box.  (The formula is ``volume =height * width * length``).
    
    - set the variables for height, width and length.
    - Calculate the volume, saving it in a variable named "volume"
    - Print your answer so it appears on the screen like this 
            "The box is *????* cubic inches."
    
.. activecode:: lps-oao2-code6
    :nocanvas:
    :nocodelens:
    :above:

    height = 18


Exercise 5.
    The box in Exercise 3 turned out to be 2592 cubic inches.  There are 1728 cubic inches in a cubic feet.  Convert the boxes volume to the decimal value of cubic feet.
    
    - set the variable "inches_per_feet" to 1728.
    - set the variable "volume" to 2592.
    - Calculate the decimal number of cubic feet and save it as a variable named "cubefeet"
    - Print your answer so it appears on the screen like this  
            "2592 cubic inches is *????* cubic feet."
    
.. activecode:: lps-oao2-code7
    :nocanvas:
    :nocodelens:
    :above:

    inches_per_feet = 1728



Exercise 6.
    Covert 523 days to an integral number of weeks and days.
    Print your answer so it appears on the screen like this  
            "523 is *????* weeks and *????* days."
    
.. activecode:: lps-oao2-code8
    :nocanvas:
    :nocodelens:
    :above:

    



.. index:: operator, operand, integer division, modular division

|
|
|

:sctnhead:`Glossary and Terms`

Division ``\``
    Decimal (floating point) division.  Results are **always a float**, even if the operands are both ints.

Integer Division ``\\``
    The result is always an integer (whole number), and **always rounded down**.  Thus ``100 // 99`` is ``9``.

Modular Division  ``%``
    Called 'mod'.  The result is the remainder from integer division. Examples:     ``4 % 3  is 1`` ,  ``100 % 9 is 1`` , ``5 % 5 is 0`` , ``422 % 211 is 0`` , ``423 % 211 is 1``
