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
   :prefix: lps-vnak-
   :start: 1


Variable Names and Keywords
---------------------------

:sctnhead:`Variable Names`

Here are the rules for naming variables:

|NOTE| :notetext:`Variable names can start with a letter or an underscore '_'`.  It is a bad idea to start a variable name with a capital letter.  By convention, a capital letter means a word is the name of a class.


|NOTE| :notetext:`Variable names can contain letters, numbers and  underscores.`

|NOTE| :notetext:`Variable names CANNOT contain spaces`.  

|NOTE| :notetext:`Upper case vs. lower case matters`.  ``hiMom`` is a different variable than ``himom``.

|NOTE| :notetext:`Variable names can't be keywords`.  Keywords are words like ``and``,``if`` and ``for``, that are reserved by python for its own use.

Some Guidelines

- The underscore character (``_``)  is often used in names with multiple words, such as ``my_name`` or ``price_of_tea_in_china``.

- Instead of underscore, some people like to use "camel case", where the beginning of new words are capitalized: ``myName``, or ``priceOfTeaInChina``.

- Don't start a variable name with a capital letter.  By convention, a capital letter means a word is the name of a class.

- There are some situations in which names beginning with an underscore have special meaning, so a safe rule for beginners is to start all names with a letter.


..

If you give a variable an illegal name, you get a syntax error.  In the example below, each of the variable names is illegal.

.. sourcecode:: python

    76trombones = "big parade"
    more$ = 1000000
    class = "Computer Science 101"


``76trombones`` is illegal because it does not begin with a letter.  

``more$`` is illegal because it contains an illegal character, the dollar sign. 

``class`` is one of the Python **keywords**. 

:sctnhead:`Keywords`

Keywords define the language's syntax rules and structure, and they cannot be used as variable names.  Python has thirty-something keywords (and every now and again improvements to Python add or eliminate one or two):

======== ======== ======== ======== ======== ========
and      as       assert   break    class    continue
def      del      elif     else     except   exec
finally  for      from     global   if       import
in       is       lambda   nonlocal not      or
pass     raise    return   try      while    with
yield    True     False    None
======== ======== ======== ======== ======== ========

You might want to keep this list handy. If the interpreter complains about one
of your variable names and you don't know why, see if it is on this list.


:sctnhead:`Naming Variables`

When choosing a variable name, |NOTE| :notetext:`use a name that will help you, and other people who read your code, to understand what the variable contains.`  If your are calculating the average of a group of numbers, give it a name like ``average``.  If you are calculating the seconds since midnight, give the variable like ``seconds``, or even ``secondSinceMidnight``.

.. caution::

    Beginners sometimes confuse  names that are meaningful to humans with having meaning to the computer. They think that if a variable is called ``average``, it will somehow automatically calculate an average, or a variable called ``pi`` will automatically have the value 3.14159.  No! The computer doesn't attach any meaning to variable names.  To the computer, they are just names.  
    
    minus_one = 100
    
    In spite of the name,  the value of minus_one is 100.


.. index:: keyword, variable names

