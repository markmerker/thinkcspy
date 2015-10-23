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

.. |MOD_LOOK| image:: Figures/mod_look.png
    
.. qnum::
   :prefix: lps-oao2-
   :start: 1


Operators and Operands: Part 2
----------------------------------------

:sctnhead:`The Three Faces of Division`

We figured out in the last lesson the three different kinds of arithmetic.  Each has a different operand to invoke it.

    Division ``/``
        Good old decimal (floating point) division.  Results are **always a float**, even if the operands are both ints.
    
    Integer Division ``//``
        The result is always an integer (whole number), and **always rounded down**.  Thus ``100 // 99 `` is ``9``, even though the decimal answer is ``9.9``, and if we were rounding it would be ``10``.  Cutting off the decimal part of the number is sometimes call
        ed **truncating**.
    
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
     
 
:sctnhead:`What is mod for?  Units, not mini-skirts`

In the sixties, one of the hottest fashion fads was called "Mod".  It was short for "modern", which, as you can see, it totally was. 

|MOD_LOOK| 

**The "mod look" has nothing to do with modulus arithmetic.**


Modulus arithmetic (AKA integer arithmetic) is really useful when we think about all the different Units we use.  We use decimal, base 10, arithmetic.  This works for money, because there are 100 cents in a dollar.  But there are:

- 2 pints in a quart
- 4 quarts in a gallon
- 12 inches in a foot
- 3 feet in a yard
- 60 seconds in a minute
- 60 minutes in an hour
- 16 ounces in a pound
- 2000 pounds in a ton

and many more measures not related to 10.  Modulus makes calculating in these units much simpler.

Take the problem:  27 quarts is how many gallons and quarts?  To do this with decimal arithmetic, we take the following steps

- Since there are four quarts in a gallon, divide  ``27 / 4``. The answer is ``6.75``. (long division = yuck)
- Throw away the .75, which leaves '6 gallons'.  How many quarts are left?
- 6 gallons  is 24 quarts  (``6 gal * 4 quarts per gallon``).  
- Subtract 24 from the original 27 quarts, and you have 3 quarts left  ``27 - 24 = 3``
- The answer is 6 gallons, 3 quarts.

Now let's try the same problem using integer arithmetic:

Since there are four quarts in a gallon
    
    - ``27 // 4 = 6``
    - ``27 % 4 = 3``
    - The answer is 6 gallons, 3 quarts.
    

How many feet and inches in 109 inches.

    - ``109 // 12 = 9``
    - ``109 % 12 = 1``
    - The answer is 9 feet, 1 inch.
    
How many tons and pounds in 34,212 pounds.

    - ``34212 // 2000 = 17``
    - ``34212 % 2000 = 212``
    - The answer is 17 tons, 212 pounds.

**Working Backwards**

Now lets try a harder one. How many yards, feet and inches in 202 inches.

    - ``202 % 12 = 10`` So there are 10 inches left over.
    - How many yards in 16 feet?  ``16 // 3 = 5`` 
    - How many feet left over after the yard?  ``16 % 3 = 1``
    - The answer is 5 yards, 1 foot, 10 inches.
    
Notice the order for this one might we different than what you expect.  Rather than trying to get yards first we get feet and inches, and then get yards from that number of feet.  

Here is an even harder one. There are 24 hours in a day, 60 minutes in an hour, 60 second in a minutes.  How long is 182405 seconds?

.. reveal:: lps-oao2-rev2
    :showtitle:Show 

    - 60 seconds per minute, so ``182405 // 60 = 3040`` , ``182405 % 60 = 5``,
            so far we have 3040 minutes, 5 seconds

    - 60 minute per hour, so ``3040 // 60 = 50``, ``3040 % 60 = 40``
            so we have 50 hours, 40 minutes, 5 seconds

    - 24 hours per day, so ``50 // 24 = 2``, ``50 % 24 = 2``
            so we have 2 days, 2  hours, 40 minutes, 5 seconds
            
:sctnhead:`Exercises`

Your exercise sheet has a lot of unit problems to solve.  The bad news is you have to solve them on paper, showing your work.  The good news is you can use the python code below to do the arithmetic.  In the code below change the values of x and itemsPerUnit, and run the program.  The code as written calculates the number of feet and inches in 45 inches.  Since ther are 12 inches in a foot, itemsPerUnit = 12. 

.. activecode:: lps-oao2-code2
    :nocodelens:

    x = 45
    itemsPerUnit = 12
    print( x // itemsPerUnit, ", ", x % itemsPerUnit  )



.. index:: operator, operand, integer division, modular division

|
|
|

:sctnhead:`Glossary and Terms`

Division ``/``
    Decimal (floating point) division.  Results are **always a float**, even if the operands are both ints.

Integer Division ``//``
    The result is always an integer (whole number), and **always rounded down**.  Thus ``100 // 99`` is ``9``.

Modular Division  ``%``
    Called 'mod'.  The result is the remainder from integer division. Examples:     ``4 % 3  is 1`` ,  ``100 % 9 is 1`` , ``5 % 5 is 0`` , ``422 % 211 is 0`` , ``423 % 211 is 1``

Twiggy
    The skinniest model of the 20th century.