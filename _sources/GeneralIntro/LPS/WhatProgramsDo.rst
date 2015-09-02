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
As we mentioned before |NOTE| :notetext:`A program is a set of instructions that tell the proccessor how to get input data, manipulate in, and create output.`  We have tried breaking up some human tasks.  Now, let's look at tasks a computer might perform.

Converting Pounds
------------------------
Here is a little program that converts pounds to kilograms.  Try it.

.. raw:: html
    <script type="text/javascript">
       function forward() {
          with (document.convert) {
         unit1.value = unit1.value.toString().replace(/[^\d\.eE-]/g,'');
         if (unit1.value*0.45359237 != 0) {
            unit2.value = unit1.value*0.45359237;
         }
          }
       }
       function backward() {
          with (document.convert) {
         unit2.value = unit2.value.toString().replace(/[^\d\.eE-]/g,'');
         if (unit2.value/0.45359237 != 0) {
            unit1.value = unit2.value/0.45359237;
         }
          }
       }
    </script>


.. raw:: html
    <form name="convert" style="font-size:1.3em;border:solid 1px #B7D7AF;border-radius:7px;background-color:#EEEEEE;margin-left:10px;margin-right:10px;padding-left:10px;padding-right:10px">
    <br />
    <table border="0" cellpadding="7" cellspacing="0">
        <tr>
            <td><input type="text"  name="unit1" size="10" maxlength="100" style="font-size:1em" onchange="forward()" value=""></td><td><strong>pounds</strong>
            </td>
        </tr><tr>
            <td><input type="text"  name="unit2" size="10" maxlength="100" style="font-size:1em" onchange="backward()" value=""></td>
            <td><strong>kg</strong></td>
        </tr><tr>
            <td>
            <input type=button value="Convert" style="font-size:1em;margin-bottom:15px" onclick="forward()">
            </td>
        </tr>
    </table>
    </form>


|
|
|

.. index:: programming,input,output, processing

