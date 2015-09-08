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
   :prefix: lps-gi-top-
   :start: 1


A Quick Taste of Python
====================

While it has many complex intracacies, some basic python code is readable, almost as if it was English.  

Here is the world's most famous program.  Since 1978 when the langauge C was published to the world, all new languages like introduce themselves by showing how write a program that outputs to the screen:

::
    
                Hello World!

|

    .. activecode:: hello_world
        :above:
        :nocodelens:

        print( "Hello world!" )

**Things to notice**

-  The data the we want the print command to use is inside of perenthesis.
-  The phrase Hello World! is surrounded by quotes.
 
 |
        
We have said that programs process data.  What is data?  Well, it is information, but that doesn't really tell us much.  Let's take some examples.  WHile there are many types of data, tehre are two you are very familiar with.  They are **numbers** and **words**.   Genereally in CS, we refer to words as **text**.  Text is anything you can type on a keyboard, including spaces, numbers, and punctuation.   
|NOTE| :notetext:`A string  is a piece of text inside a pair of quotes.` A string can be as short as a single space **" "**, or even empty "".  It can be as long hundreds characters - 

::

"Here is an extremely long string which is created to demonstrate that strings can be of great length, contain text numbers like 42, primitive emoticons :) and p_u^n%c#t!u)a*t?i>o<n marks of all kinds.  I could go on like this for a long time, but it might become uninteresting."

|

:sctnhead:`Numbers`

Here is program that process numbers.  Predict what it will do, and then press "Run".


    .. activecode:: lps-gi-top-code-1
        :above:
        :nocodelens:

        x = 1
        y = 2
        z = x + y
        print( x, "+", y, "=", z )
        
**Things to notice**

-   The print statement prints a list of things, separated by commas.
-   The print statement prints both numbers (like x) with text like ("="). 
-   Text, like the plus sign **(+)**, is surrounded by quotes.
-   **Variables** are things that computer uses to keep track of a value.  Here we see the program setting a variable called x to the number 1.  It can then use x later,  as in the addition z = x + y, and as in the print statement.  Because x was set to 1, wherever it appears later, it is as if the number a 1 was there.

**Exercise 1.** Modify the program above by changing the values x and y are set to, and see what happens.

|

**Exercise 2.**  Add to the program below so that it prints not only the results of addition of a and b, but also subtraction, multiplication (*), and division (/).   When you have this program working properly, press the "Save" button, and your program will submitted to your teachers.

    .. activecode:: lps-gi-top-code-2
        :above:
        :nocodelens:

        a = 1
        b = 2
        c = a + b
        print( a, "+", b, "=", c )
        c = a - b
        

|

:sctnhead:`Text`

Here is a program that processes text


    .. activecode:: lps-gi-top-code-3
        :above:
        :nocodelens:

        myName = "Mark Merker"
        print( "Hello", myName )

**Things to notice**

-   This time we used a variable named myName
-   Instead of setting the value of the variable to a number, we set it to text. 

Modify the code above to use your name, and a greeting other than "Hello".  When it is working properly, press "Save" to submit it.


.. index:: numbers,text,words,processing,hello world, strings
