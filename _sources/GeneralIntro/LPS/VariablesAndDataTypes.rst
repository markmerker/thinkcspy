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
   :prefix: lps-vadt-
   :start: 1

Variables and Data Types
-----------------------------------------

|NOTE| :notetext:`A Variable is a named entity that holds a value.`  There are many different types of values.  Last lesson we talked about Text and Numbers.   In python, these are actually three types of data: strings, integers and decimal numbers.  These types have the following names in python:

+-------------------+------------+------------+
| Data Type         | Python Type| Samples    |
+===================+============+============+ 
| text or strings   | str        | "hi mom"   | 
+-------------------+------------+------------+ 
| integers or whole | int        | 42 -4 201  | 
| numbers           |            |            |  
+-------------------+------------+------------+ 
| decimals or       | float      | 42.0 123.19| 
| floating point    |            |            |  
+-------------------+------------+------------+ 


:sctnhead:`Why Data Types Matter`
    When you create a variable, the computer needs to store its value in memory.  It also needs to be ready to process its value in different ways.  But an int needs to be stored differently than a float, which is stored differently than a string. An int is stored in 4 bytes (32 bits).  A floating point number takes 64 bits.  The meaning of each bit in the different numbers is completely different.  A string is stored roughly with 1 byte for each character.  All ints require the same 4 bytes, but a string requires as many bytes as there are characters.
    
    The computer needs the type so it can now how to store the data, and how to manipulate it.


The python names of the types are important for two reasons.  There is a python function named **type**, that will tell you the type of any variable.  In addition, you can convert a variable from one type to another by using the type name as function.

The python code below demonstrates these functions:

    .. activecode:: lps-vadt-code-1
        :above:
        :nocodelens:

        a = 1.0
        typea = type(a)
        print ( "a is ", a, " type ",typea  )
        a = int( a )
        typea = type(a)
        print ( "a is ", a, " type ",typea  )
        a = str( a )
        typea = type(a)
        print ( "a is ", a, " type ",typea  )
        a = float( a )
        typea = type(a)
        print ( "a is ", a, " type ",typea  )

**Things to notice**

-  We use the equal sign **=** to set the value of a variable.  This is called **assignment**.
-  In the first line, **a** is set to a float, because the number has a decimal point.
-  The **type()** function creates a string with the word **class** followed by the variable's type.
-  When we change **a**'s type to int, it's display value changes. 


:sctnhead:`Converting Data Types`


Some data types can be converted to others, some can't. For example, if you try this

..
 
    int( "hi mom") 
    
you will get an error, because there is no way to convert "hi mom" to an integer.      
    
    
**Exercise 1.** In this exercise, you are going to test what can be converted to what without an error.  You have an exercise sheet that will tell you what conversions to try.  As you test different conversions, write your results in on the exercise sheet.  When you have tested all the combinations, save your code, so the teachers can see it.

.. activecode:: lps-vadt-code-2
    :above:
    :nocodelens:

    #  Testing int to float
    a = 1
    print ("Testing int to float by converting a of value ", a )
    a = float( a )
    print ("  -- result  a is ", a, " type is", type(a) )
    print()

..


|
|

:sctnhead:`Glossary and Terms`

assignment
    setting the value of a variable with an equal sign.

type
    python name and function for the data type of an item.
    
int
    python data type for integers, whole numbers.
    
float
    python data type for decimal or floating point numbers.
    
str
    python data type for text strings.