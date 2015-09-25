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
   :prefix: lps-ooo-
   :start: 1



Order of Operations  -  PEMDAS
---------------------------------------

Suppose we want to find the ``average of four numbers, 1, 2, 3, and 7`` or we want to take the ``square root of 625``, we might write

.. activecode:: lps-ooo-code1
    :nocanvas:
    :nocodelens:
    
    print( 1 + 2 + 3 + 7 / 4 )
    print( 625 ** 1/2 )


Unfortunately the answers you get will be wrong.  In the first case python adds 1 + 2 + 3 + seven fourths.  In the second case it raises 625 to the first power, and divides it by 2.

Fix the above code using parenthesis.

When more than one operator appears in an expression, the order of evaluation
depends on the **rules of precedence**. Python follows the same precedence
rules for its operators that mathematics does.


The acronym **PEMDAS** is a useful way to remember the order of operations.  Here they are by priority

#. **Parentheses** ``()`` have the highest precedence.  They can be used to force an
   expression to evaluate in the order you want, as we saw above.
   
   You can also use parentheses to make an expression easier to read, as in
   ``(minute * 100) / 60``, even though it doesn't change the result. *It is a good idea to use parenthesis ofen, to make your code clear both to yourself and others.*
#. **Exponents** have the next highest precedence, so ``2**1+1`` is 3 and
   not 4, and ``3*1**3`` is 3 and not 27.  Can you explain why?
#. **Multiplication** ``*`` and **Division** ``/ // %`` operators have the same 
   precedence, which is higher than addition and subtraction, which
   also have the same precedence. So ``2*3-1`` yields 5 rather than 4, and
   ``5-2*2`` is 1, not 6.
#. **Addition** ``+`` and **subtraction** ``-`` are the lowest precedence.

**Operators with the same precedence are evaluated from left-to-right.** 
   So ``6-3+2``, the subtraction happens first, yielding 3.
   We then add 2 to get the result 5. If the operations had been evaluated from
   right to left, the result would have been ``6-(3+2)``, which is 1.


.. note::

    Due to some historical quirk, an exception to the left-to-right
    left-associative rule is the exponentiation operator `**`. A useful hint
    is to always use parentheses to force exactly the order you want when
    exponentiation is involved:

    .. activecode:: lps-ooo-code2
        :nocanvas:

        print(2 ** 3 ** 2)     # the right-most ** operator gets done first!
        print((2 ** 3) ** 2)   # use parentheses to force the order you want!

:sctnhead:`Exercise`

Write the answers to the problems in the exercise sheet.  Then enter the expression in python.  Compare your answer to pythons answer.  Make notes about your mistakes. 

.. index:: PEMDAS, precedence

|
|
|

:sctnhead:`Glossary and Terms`

PEMDAS 
    Acronym for order of precedence: **P**arenthesis, **E**xponents, **M**ultiplication and **D**ivision,  **A**ddition and **S**ubtraction.

Precedence
    The priority in which operators are applied when evaluating an expression.