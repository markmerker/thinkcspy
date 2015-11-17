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
   :prefix: lps_u2lab-
   :start: 1



Unit 2 Lab 2 - Using Codelens
==================================


**Exercise 1. Powers**

    
.. activecode:: lps_u2lab2_code1
    :above:

    def power( num, exponent):
        x = num ** exponent
        return x

    x = 3; y = 2; 
    x = power (x, y )
    x = power (x, y )
    x = power (x, y )
    x = power (x, y )
    print ( "x is",x)

**Exercise 2. Cool cats**
    
.. activecode:: lps_u2lab2_code2
    :above:
    
    def con_cat( a, b):
        c = a + " " + b
        return c

    s1 = "hi";  s2 = "mom" 
    s1 =  con_cat( s1, s2 )
    s2 =  con_cat( s1, s2 )
    s1 =  con_cat( s1, s2 )
    s2 =  con_cat( s1, s2 )
    print ( "s1 is", s2)


**Exercise 3. Add nauseum**

    
.. activecode:: lps_u2lab2_code2
    :above:


    def addEm( a, b):
        c = a + b
        return c

    a = 2;  b = 5
    a = addEm ( a, b )
    a = addEm ( a, b )
    b = addEm ( a, b )
    b = addEm ( a, b )
    a = addEm ( a, b )
    b = addEm ( a, b )
    print ("a =",a,"b =",b) 

|
|
|
:sctnhead:`Play Ground`

Do what you like and save it. Use this for practice exercise as well.

.. activecode:: lps_u2lab2_play
    :above:



.. index:: object, module
|
|

