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


|NOTE| :notetext:`There is a python function named "type", that will tell you the data type of any variable.`  

The python code below demonstrates the function:

    .. activecode:: lps-vadt-code-1
        :above:
        :nocodelens:
        :nocanvas:

        a = 1.0
        b = 10
        c = "10"
        print ( "a: value is ", a, " type is ",type(a)  )
        print ( "b: value is ", b, " type is ",type(b)  )
        print ( "c: value is ", c, " type is ",type(c)  )



**Things to notice**

-  We use the equal sign **=** to set the value of a variable.  This is called **assignment**.
-  In the first line, **a** is set to a float, because the number has a decimal point.
-  The *type()* function returns a string of the format
        ``<class 'TYPE' >`` where *TYPE* is int, float, etc.

:sctnhead:`A quick word on Functions`

    We have started to use the word ``function`` frequently, but haven't really defined it.  We are not going to define it yet, but by using it you can see how it works. A function is code that does some job.  You call it from your code.  After the name of the function are always parens (), that hold the data you want the function to use.  So saying 
    
        type( *something* )
    
    is like saying: tell me the type of *something*.
    
    Another example of a function is ``abs()``, which calculates the absolute value of a number.  So saying:
    
        abs( -23.43 )
        
    is like saying "tell me the absolute value of -23.43".  The function returns the value ``23.43``.   Quick: what is the data type of ``23.43``? 


:sctnhead:`Converting Data Types`

The name of a data type may also be the name of a function that converts data to that data type.  For example the statement

    b = int( 1.0 )

loads ``b`` with the result of converting the float 1.0 to an integer.  The value of 
``b`` becomes 1, and the data type of ``b`` is int.

Some data types can be converted to others, some can't. For example, if you try this

..
 
    int( "hi mom") 
    
you will get an error, because there is no way to convert "hi mom" to an integer.      
    
    
**Exercise 1.** In this exercise, you are going to test what can be converted to what without an error.  You have an exercise sheet that will tell you what conversions to try.  As you test different conversions, write your results in on the exercise sheet.  When you have tested all the combinations, save your code, so the teachers can see it.

.. activecode:: lps-vadt-code-2
    :above:
    :nocodelens:

    a = 14398
    b = float( a )
    print ( "a: value is ", a, " type is ",type(a)  )
    print ( "b: value is ", b, " type is ",type(b)  )


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
    
functions we have encountered
    print(),  type(),  abs(), str(), int(), float()
    
   