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
   :prefix: lps-com-
   :start: 1

Comments
--------

As programs get bigger and more complicated, they get more difficult to read.
Formal languages are dense, and it is often difficult to look at a piece off
code and figure out what it is doing, or why.
For this reason, it is a good idea to add notes to your programs to explain in
natural language what the program is doing.  These notes are called comments. 

A **comment** in a computer program is text that is intended only for the human
reader - it is completely ignored by the interpreter.
In Python, the `#` token starts a comment.  The rest of the line is ignored.
Here is a new version of *Hello, World!*.

.. activecode:: ch01_3

    #---------------------------------------------------
    # This demo program shows off how elegant Python is!
    # Written by Joe Soap, December 2010.
    # Anyone may freely copy or modify this program.
    #---------------------------------------------------

    print("Hello, World!")     # Isn't this easy!

Notice that when you run this program, it still only prints the phrase Hello, World!  None of the comments appear.
You'll also notice that we've left a blank line in the program.  Blank lines
are also ignored by the interpreter, but comments and blank lines can make your
programs much easier for humans to parse.  Use them liberally!

**Check your understanding**

.. mchoice:: question1_12_1
   :answer_a: To tell the computer what you mean in your program.
   :answer_b: For the people who are reading your code to know, in natural language, what the program is doing.
   :answer_c: Nothing, they are extraneous information that is not needed.
   :answer_d: Nothing in a short program.  They are only needed for really large programs.
   :correct: b
   :feedback_a: Comments are ignored by the computer.
   :feedback_b: The computer ignores comments.  It’s for the humans that will “consume” your program.
   :feedback_c: Comments can provide much needed information for anyone reading the program.
   :feedback_d: Even small programs benefit from comments.

   What are comments for?


Let's take a look at some exercises from the previous lesson, but this time with comments.


**Exercise A.**
    Find the average of the numbers  ``27.1, 18.5, 0 and 19``.  When you write the code, follow these steps
    
    
Answer 1.

.. activecode:: lps-com-code2
    :nocodelens:

    # add the numbers
    total = 27.1 + 18.5 + 0 + 19

    # divide by 4 because there are 4 numbers
    average = total / 4
    # outout result.
    print( "The average is", average )


Admittedly, these may be more comments than you need, but they certainly make clear the logic behind the code.

Try doing the next exercise, this time commenting your code. 


**Exercise B.**

The time is 9:23:00 AM.  How many seconds has it been since midnight?

.. activecode:: lps-com-code2
    :nocodelens:

    # calculate the total minutes since midnight
    

    # convert the minutes to seconds
    
    
    # output to screen "The number of seconds since midnight is ???".

    

..


.. index:: #, comments

