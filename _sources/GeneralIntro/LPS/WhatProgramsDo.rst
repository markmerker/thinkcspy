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

.. qnum::
   :prefix: lps-intro-2-
   :start: 1

What Programs Do
==============
|NOTE| :notetext:`A program is a set of instructions that tell the proccessor how to get input data, manipulate in, and create output.` These instructions are written in one of many Programming Languages.  But before getting into details about what a language is, and how it works, lets take just talk a little about how someone does a task.

Performing  Tasks
--------------------
Suppose I ask you to make a reservation for dinner tonight at a restaurant.  Take a minute, and list the steps you will need to take to do this.  (There is no one right answer, just name the needed steps.)

.. reveal:: lps-intro-3-rev1
    :showtitle: Show List
    :hidetitle: Hide List

        1 Ask what time, what restaurant, and how many people are going.

        2 Look up the restaurant on your phone.

        3 Call the restauant

        4 Make the reservation

Now lets make this list a little more detailed by separating and identifying your "input" steps from your "output" steps. For example,  asking a question is an output task, but getting the answer is an input task.  List the steps again.

.. reveal:: lps-intro-3-rev2
    :showtitle: Show List
    :hidetitle: Hide List

        
        1. Ask what time, what restaurant, and how many people are going. (*output*)
        
        2. Listen to my answers.  (*input*)
        
        3. You decide the time is too early (*processing*)
        
        4. Listen to my answer.  (*input*)

        5. Ask if you can make it an hour later. (*output*)

        6. Look up the restaurant on your phone. (*input*)

        7. Call the restaurant. (*output*)

        8. Ask for the reservation. (*output*)
        
        9. Make sure the restaurant confirms. (*input*)

  Notice we threw in something new.  A step where you make a decision, and we labelled it **processing**. You are not inputting or outputting, but thinking about the data (in this case, the time I suggested for dinner).
|

You  are at the train ticket window, and need buy a ticket for Boston leaving this evening.  If it is less that $30, you will buy a first class ticket.  List the steps in buying your ticket, labelling each step *input*, *output* or *processing*.


|
|
|

.. index:: programming,input,output, processing

