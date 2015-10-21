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
   :prefix: lps-input-
   :start: 1

Print & Input 
---------------

Print
======

We have used the ``print()`` function for a while now.  Let's take a close look at how it works.  ``print`` can take from zero to as many expressions as you like.  Each of these expressions is separated by a comma. ``print`` will output the evaluation of each expression to the monitor, separated by spaces.

    print( *expression*, *expression*, *expression*, ... )
    
While we have used mostly simple expressions, like strings, numbers and variables, any legal expression can be used.  Here are some complicated expressions we have looked earlier in Unit One::

    1 + 3.45 + 21
    "hello" + " " + "goodbye"
    hi + mom
    abs(-12) + abs(12)
    str( 19 ) + str ( 23.8 )
    1+2+3+4+5+6+7+8+9+10
        
Any of these expressions can be used in a print statement. 
 
What will this code output to the screen?
 
.. activecode:: lps_input_code1a

    hi = 12
    mom = 13 
    print("Hello", 1 + 3.45 + 21, "hello" + " " + "goodbye",
        hi + mom, str( 19 ) + str ( 23.8 ),  abs(-12) + abs(12),
        1+2+3+4+5+6+7+8+9+10 )
        
**Things to notice**

- Any expression can be put in a print statement

- If a statement isn't finished (for example, parens aren't closed), it can be continued on another line.  


:sctnhead:`Input`

The ``input`` function prompts the user, and returns thir response.

.. sourcecode:: python

    n = input("Please enter your name: ")

This code will put up a dialogue box.  Whatever the user types will be loaded into the variable by the assingment operator ``=``.  Try it.

.. activecode:: lps_input_code2

    n = input("Please enter your name: ")
    print("Hello", n)


*What would happen if we invoke input, but don't store the result in a variable?*  

The dialogue box would run, but the user's answer would never be stored anywhere. It would be as if it never ran.

.. activecode:: lps_input_code3

    n = ""
    input("Please enter your name: ")
    print("Hello", n)


It is very important to note that |NOTE| :notetext:`the input function always returns a string value`, (data type ``str``).  Even if you asked the user to enter their age, you would get back a string like ``"17"``, not the integer 17.  **Since a string is returned, if you want a number, you must convert the type (to ``int`` or ``float``) before using it.**


Consider this program, which we have seen before:  

.. sourcecode:: python

    total_time = 987
    minutes = total_time // 60
    seconds = total_time % 60
    print( total_time , "seconds is", minutes , "minutes and", seconds , "seconds." )

Let's change this program so that the user can input the total time value.  We prompt the user for a value, but then we must convert the string to an integer.  From there the process is the same as before.  

.. activecode:: lps_input_code4

    str_seconds = input("Please enter the number of seconds you wish to convert")
    total_time = int( str_seconds)
    minutes = total_time // 60
    seconds = total_time % 60
    print( total_time , "seconds is", minutes , "minutes and", seconds , "seconds." )

The variable ``str_seconds`` refers to the strings that is entered by the user. If your code said ``minutes = str_seconds // 60``, it would cause an error, because you would be dividing a string by an integer.


.. mchoice:: test_question2_7_1
   :answer_a: &lt;class 'str'&gt;
   :answer_b: &lt;class 'int'&gt;
   :answer_c: &lt;class 18&gt;
   :answer_d: 18
   :correct: a
   :feedback_a: All input from users is read in as a string.
   :feedback_b: Even though the user typed in an integer, it does not come into the program as an integer.
   :feedback_c: 18 is the value of what the user typed, not the type of the data.
   :feedback_d: 18 is the value of what the user typed, not the type of the data.

   What is printed when the following statements execute?

   .. code-block:: python

     n = input("Please enter your age: ")
     # user types in 18
     print ( type(n) )



Try it by pressing "Show"

.. reveal:: lps-input-rev2
    :showtitle:Show 

    .. activecode:: lps_input_code3
    
        # user should type in 18
        n = input("Please enter your age: ")
        print ( type(n) )

    

.. index:: input, print, expression

|
|
|

:sctnhead:`Glossary and Terms`

input
    A function that gets user keyboard input.

