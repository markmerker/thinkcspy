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
   :prefix: lps-gi-wpd-
   :start: 1

  
What programs Do
====================
As we mentioned before |NOTE| :notetext:`A program is a set of instructions that tell the proccessor how to get input data, manipulate in, and create output.`  We have thought a little about the steps a person takes when they perform a task.  Now lets thinks about steps programs perform to accomplish a task


Converting Pounds to Kilos
------------------------------- 
Here is a little program that converts pounds to kilograms.  Press Run to try it.

    .. activecode:: lps-gi-wpd-code-1
        :above:
        :hidecode:
        :nocodelens:

        def main()  :  
            choice = ''
            factor = .45
            pounds = float( input( "Enter the number of pound to convert to kilos: " ) )
            print ( "%s pounds is  %s kilos" % (pounds,  round(pounds*factor,2) ))

            kilos = float( input( "Enter number of kilos to convert to pounds: " ) )
            print ( "%s kilos is  %s pounds" %  (kilos, round(kilos / factor,2) ))


        main()

|
|
Now lets create list of input, output and processing steps the program may have used to perform this task.

.. reveal:: lps-gi-wpd-rev-1
    :showtitle: Show List
    :hidetitle: Hide List

    #. Ask user for the number of pounds.  *(output)*
    
    #. Read users response *(input)*
    
    #. Ask user for the number of kilos.  *(output)*
    
    #. Read users response *(input)*
    
    #. Calculate the kilos and pounds  *(processing)*
    
    #. Display results to user. *(output)*


.. index:: programming,input,output, processing

