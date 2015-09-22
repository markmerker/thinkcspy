..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


THE BOOK STOPS HERE
================

This book is a rewrite (for the classroom) of Think Like a Computer Scientist.  The re-write has only gone this far.  The rest is the original book.


When a variable name appears in the place of an operand, it is replaced with
the value to which it refers.
For example, what if we wanted to find length in miutes of a movie that was 2 hours and 23 minutes long, we might write the following code.

.. activecode:: lps-oao-code-2
    :nocanvas:
    :nocodelens:

    hours = 2
    minutes = 23
    total_minutes = (hours * 60) + minutes
    print( total_minutes )

