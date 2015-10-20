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

Input
------

Consider this program, which we have seen before.  

.. sourcecode:: python

    total_time = 987
    minutes = total_time // 60
    seconds = total_time % 60
    print( total_time , "seconds is", minutes , "minutes and", seconds , "seconds." )

What does it calculate?

This program works fine but it only works with one value, 987.  What if we wanted to rewrite the program so the user can enter any value they wish for the number of seconds.  The program could then print the proper result for that user-entered value.

In order to do this, we use built-in function called ``input``.  Here is a simple example of ``input``.

.. sourcecode:: python

    n = input("Please enter your name: ")

The input function allows the user to provide a **prompt string**.  When the function is executed, it creates a prompt box on the screen, with the prompt, and a place for the user to enter their input. 

.. activecode:: lps_input_code2

    n = input("Please enter your name: ")
    print("Hello", n)

It is very important to note that the ``input`` function returns a **string** value, (type ``str``).  Even if you asked the user to enter their age, you would get back a string like ``"17"``, not the integer 17.  **Since a string is returned, if you want a number, you must convert the type (to ``int`` or ``float``) before using it.**

To modify our previous program, we will add an input statement to allow the user to enter the number of seconds.  Then we will convert that string to an integer.  From there the process is the same as before.  

.. activecode:: lps_input_code2

    str_seconds = input("Please enter the number of seconds you wish to convert")
    total_time = int( str_seconds)
    minutes = total_time // 60
    seconds = total_time % 60
    print( total_time , "seconds is", minutes , "minutes and", seconds , "seconds." )

The variable ``str_seconds`` refers to the strings that is entered by the user. If your code said ``minutes = str_seconds // 60``, it would cause an error, because you would be dividing a string by an integer.


**Check your understanding**

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


.. index:: input

