..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. |NOTE| image:: ../../_static/LPS/pencil.png

.. role:: notetext

.. raw:: html

    <style> .notetext {color:green; font-weight: bold; font-size: 110%; } </style>

.. role:: sctnhead

.. raw:: html

    <style> .sctnhead {color:black; font-weight: bold; font-size: 140%; } </style>
    
.. qnum::
   :prefix: lps_gc_
   :start: 1


8. Get creative
-------------------------

In the previous lessons, we have learned some important principals about coding.  We have learned a number of turtle graphics commands we can use to draw with.  We have seen that functions can use other functions.  We have seen that a for loop can repeat operations any number of times.

Now, we can use these things to create our own drawings.  Below is a list of all the turtle functions we have already used.  It is followed by a list of new functions.  The new functions have test areas where try them out: see how they work with different parameters.

Once you have tried the new functions, you are ready to start creating your own pictures.   You have five different code boxes in which to draw a picture.  The are all loaded with the utility functions.

Once you have some work you like, be sure to save it.  If you want to try something different, try another code box.

**Built-in Turtle Functions wWe Have Used** 

=========== =============== ============== =============================================================================================================   
Function    Parameters       Examples       Notes 
                                           
=========== =============== ============== =============================================================================================================   
forward     steps           forward(50)    Move forward *steps* pixels.
backward    steps           backward(18)   Move forward *steps* pixels.
right       degrees         right(30)      Turn right by the number of *degrees*
left        degrees         left(30)       Turn left by the number of *degrees*
setheading  degrees         setheading(45) Point turtle degrees from east (right).0 points right, 45 points toward the top-right, 90 straight up, etc.
pendown                     pendown()      Put pen to paper, e.g. draw when turtle moves.
penup                       penup()        Lift pen from paper, e.g. don't draw when turtle moves.
pensize     pixels          pensize(12)    Make pen *pixels* wide.
color       name            color("red")   Set pen color to a name. Some names work, some don't.
color       r,g,b           color(1,5,9)   Set color using values from 0 to 255 for red, green and blue.
=========== =============== ============== =============================================================================================================   

**Other Built-in Turtle Functions** 

=========== =============== =================== ==========================================================================================================================   
Function    Parameters       Examples           Notes 
                                           
=========== =============== =================== ==========================================================================================================================   
circle      radius          circle(25)          Draw a circle with size *radius* 
dot         size, color     dot(15,"red")       Draw a filled circle with diameter size, and of the requested color
fillcolor   color           fillcolor("red")    Use this color when filling a shape.
begin_fill                  begin_fill()        Call this before you start to draw a shape you want filled.
end_fill                    end_fill()          Draw this after you draw a shape you want filled, and the shape will fill.
shape       shapeName       shape("turtle")     Change the appearance of the turtle.  Build in shapes are "arrow", "turtle", "circle", "square", "triangle", "classic"
stamp                       stamp()             Print the image of the turtle on the screen.
randint     low,high        randint(-200,200)   Return a random integer between low and high.
=========== =============== =================== ==========================================================================================================================   

**LPS Provided Turtle Functions** 

============== ======================= ==================== ==========================================================================================================================   
Function       Parameters              Examples             Notes 
                                           
============== ======================= ==================== ==========================================================================================================================   
moveTurtle     x,y                     moveTurtle(-150,100) Pick up pen, move it x,y, then lower pen.
drawPolygon    sides,size              drawPolygon(8,25)    Draw a polygon with 'sides' number of sides, each 'size' pixels long
drawCurve      steps,size,degrees      drawCurve( 30,4,3)   Draw a curve, degrees steep, with 'step' segments, each 'size' long.  use minus degrees to curve to the right.
drawSpiral     steps,initSize,degrees  drawSpiral( 20,5,45  Draw a curve, degrees steep, with 'step' segments, the first being 'size' long.  Use minus degrees to curve to the right.
drawStar       points, size            drawStar( 5, 30 )    Draw a flake-like star, each branch size long.
drawStar1      points, size            drawStar( 5, 30 )    Draw a regular star, only works for odd number of points.
setRandomColor                         setRandomColor       Set turtle to a random color
============== ======================= ==================== ==========================================================================================================================   

Sample Code
=============

Here lots of code snippets that use the python functions,  Scroll to the bottom
each code box, and look at the area with the comment ## SAMPLE CODE ##

**Using draw star**


.. activecode:: lps_gc_sample_1
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def drawStar( points, size ):
        angle = 360.0 / points
        for i in range( points):
            tur.forward( size )
            tur.back( size )
            tur.left( angle )


    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
        # draw a simple 9 pointed star
    moveTurtle( -100, 0 )
    drawStar( 9, 100 )
    
        # draw a multicolor star
    moveTurtle( 100, 0 )
    width = 16
    for color in ["blue", "red", "yellow","green" ]:
        tur.color( color )
        tur.pensize( width )
        drawStar( 20, 100 )
        width = width - 4
      
**Getting random: using randint and setRandomColor**


.. activecode:: lps_gc_sample_2
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def drawStar( points, size ):
        angle = 360.0 / points
        for i in range( points):
            tur.forward( size )
            tur.penup()
            tur.back( size )
            tur.pendown()
            tur.left( angle )
    
    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))


    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
    tur.pensize(2)
    for i in range(25):
        x = randint(-200,200)
        y = randint(-200,200)
        size = randint(25,40)
        points = randint(6,8)
        moveTurtle( x, y)
        setRandomColor()
        drawStar( points, size )
        
**More Stars: drawStar1 and drawPolygon**


.. activecode:: lps_gc_sample_3
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    
    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))


    def starAngle( numSides ):
        a = getInternalAngle( numSides )
        if (numSides % 2) == 1 :
            angle = (180 - a) / 2.0
        else:
            angle = 180 - a
        return angle

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)

    def drawStar1(  sideCount,  sideSize ):
        tur.pendown()
        angle = starAngle( sideCount )
        tur.left( 90 - (angle / 2) )
        for i in range( sideCount ):
            tur.forward( sideSize )
            tur.right( 180 - angle)

    def drawPolygon( sides, size):
        # get internal angle
        internalAngle = getInternalAngle( sides )
        for i in range( sides ):
            tur.forward( size )
            tur.left( 180 - internalAngle )


    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
    tur.pensize(2)
    x = -150
    y = -150
    points = 5
    polyside = 5
    for i in range(6):
        moveTurtle( x, y)
        tur.setheading(0)
        x = x + 50
        y = y + 50
        size = 60
        polysize = 15
        setRandomColor()
        drawStar1( points, size  )
        setRandomColor()
        drawPolygon( polyside, polysize )
        points = points + 4
        polyside = polyside + 1
        


**Using Curves: drawCurve**


.. activecode:: lps_gc_sample_4
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    
    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))

    def  drawCurve( steps, size, degrees ):
        for i in range( steps ):
            tur.forward( size )
            tur.left( degrees ) 


    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
    tur.pensize(2)
    moveTurtle( -150, -150)
    tur.pensize(2)
    moveTurtle( -150, -150)
    setRandomColor()
    drawCurve( 20, 5, 3)
    setRandomColor()
    drawCurve( 20, 5, -3)

    setRandomColor()
    drawCurve( 20, 5, 10)
    setRandomColor()
    drawCurve( 20, 5, -10)

    x = -150
    y = 0
    degrees = -2.5
    width = 15
    steps = 35
    size = 10
    tur.pensize( width )
    for color in ["violet","indigo","blue", "green","yellow","orange","red"]:
        moveTurtle( x, y )
        tur.setheading(45)
        tur.color( color )
        drawCurve( steps, size, degrees )
        y = y - width
        
    
**Using Curves: drawSpiral**


.. activecode:: lps_gc_sample_5
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))

    def drawSpiral( steps, initSize, degrees  ):
        size = initSize
        for i in range( steps ):
            tur.forward( size )
            size = size + 1
            tur.left( degrees )
        

    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
    steps = 60
    degrees = 30
    size = 3
    tur.pensize(10)
    setRandomColor()
    drawSpiral( steps, size, degrees )
    moveTurtle( 0, 0 )
    tur.setheading( 0 )
    setRandomColor()
    tur.pensize(5)
    drawSpiral( steps, size, degrees )
   

**Fill: begin_fill, end_fill, fillcolor**


.. activecode:: lps_gc_sample_6
    :above:
    :nocodelens:
    
    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)

    def drawStar1(  sideCount,  sideSize ):
        tur.pendown()
        angle = starAngle( sideCount )
        tur.left( 90 - (angle / 2) )
        for i in range( sideCount ):
            tur.forward( sideSize )
            tur.right( 180 - angle)

    def drawPolygon( sides, size):
        # get internal angle
        internalAngle = getInternalAngle( sides )
        for i in range( sides ):
            tur.forward( size )
            tur.left( internalAngle )
        
    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def starAngle( numSides ):
        a = getInternalAngle( numSides )
        if (numSides % 2) == 1 :
            angle = (180 - a) / 2.0
        else:
            angle = 180 - a
        return angle


    ## SAMPLE CODE ##
    ## SAMPLE CODE ##
    
    moveTurtle( -150, -150 )
    tur.fillcolor( "red" )
    tur.begin_fill()
    drawPolygon( 4, 80 )
    tur.end_fill()
    
    moveTurtle( -75, -75 )
    tur.setheading( 0 )
    tur.fillcolor( "blue" )
    tur.begin_fill()
    drawStar1( 7, 80 )
    tur.end_fill()
    
    moveTurtle( 0, 0)
    tur.setheading( 0 )
    tur.fillcolor( "green" )
    tur.color( "green" )
    tur.begin_fill()
    drawPolygon( 8, 100 )
    tur.end_fill()
    
   
Draw Your Picture
==================

Here are three code boxes to try different pictures.

Be sure to save your work as you go along.


.. activecode:: lps_gc_code_1
    :above:
    :nocodelens:
    

    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)


    def drawPolygon( sides, size):
        # get internal angle
        internalAngle = getInternalAngle( sides )
        for i in range( sides ):
            tur.forward( size )
            tur.left( 180 - internalAngle )

    def drawCurve( steps, size, degrees ):
        for i in range( steps ):
            tur.forward( size )
            tur.left( degrees ) 

    def drawSpiral( steps,initSize,degrees  ):
        size = initSize
        for i in range( steps ):
            tur.forward( size )
            size = size + 1
            tur.left( degrees )

    def drawStar( points, size ):
        angle = 360.0 / points
        for i in range( points):
            tur.forward( size )
            tur.back( size )
            tur.left( angle )

    def starAngle( numSides ):
        a = getInternalAngle( numSides )
        if (numSides % 2) == 1 :
            angle = (180 - a) / 2.0
        else:
            angle = 180 - a
        return angle

    def drawStar1( sideCount,  sideSize ):
        if (sideCount % 2) == 0:
            return
        tur.pendown()
        angle = starAngle( sideCount )
        tur.left( 90 - (angle / 2) )
        for i in range( sideCount ):
            tur.forward( sideSize )
            tur.right( 180 - angle)

    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur
    
    
.. activecode:: lps_gc_code_2
    :above:
    :nocodelens:


    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)


    def drawPolygon( sides, size):
        # get internal angle
        internalAngle = getInternalAngle( sides )
        for i in range( sides ):
            tur.forward( size )
            tur.left( 180 - internalAngle )

    def drawCurve( steps, size, degrees ):
        for i in range( steps ):
            tur.forward( size )
            tur.left( degrees ) 

    def drawSpiral( steps,initSize,degrees  ):
        size = initSize
        for i in range( steps ):
            tur.forward( size )
            size = size + 1
            tur.left( degrees )

    def drawStar( points, size ):
        angle = 360.0 / points
        for i in range( points):
            tur.forward( size )
            tur.back( size )
            tur.left( angle )

    def starAngle( numSides ):
        a = getInternalAngle( numSides )
        if (numSides % 2) == 1 :
            angle = (180 - a) / 2.0
        else:
            angle = 180 - a
        return angle

    def drawStar1( sideCount,  sideSize ):
        if (sideCount % 2) == 0:
            return
        tur.pendown()
        angle = starAngle( sideCount )
        tur.left( 90 - (angle / 2) )
        for i in range( sideCount ):
            tur.forward( sideSize )
            tur.right( 180 - angle)

    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur



.. activecode:: lps_gc_code_3
    :above:
    :nocodelens:
    

    import turtle          
    import random
    from random import randrange
    from random import randint

    wn = turtle.Screen()  
    tur = turtle.Turtle()
    tur.speed(300)

    def moveTurtle( x, y ):
        tur.penup()
        tur.goto( x, y )
        tur.pendown()

    def setRandomColor():
        tur.color( randint(0,255), randint(0,255), randint(0,255))

    def getInternalAngle( sides ):
        return ( 180 * (sides-2)) / float(sides)


    def drawPolygon( sides, size):
        # get internal angle
        internalAngle = getInternalAngle( sides )
        for i in range( sides ):
            tur.forward( size )
            tur.left( 180 - internalAngle )

    def drawCurve( steps, size, degrees ):
        for i in range( steps ):
            tur.forward( size )
            tur.left( degrees ) 

    def drawSpiral( steps,initSize,degrees  ):
        size = initSize
        for i in range( steps ):
            tur.forward( size )
            size = size + 1
            tur.left( degrees )

    def drawStar( points, size ):
        angle = 360.0 / points
        for i in range( points):
            tur.forward( size )
            tur.back( size )
            tur.left( angle )

    def starAngle( numSides ):
        a = getInternalAngle( numSides )
        if (numSides % 2) == 1 :
            angle = (180 - a) / 2.0
        else:
            angle = 180 - a
        return angle

    def drawStar1( sideCount,  sideSize ):
        if (sideCount % 2) == 0:
            return
        tur.pendown()
        angle = starAngle( sideCount )
        tur.left( 90 - (angle / 2) )
        for i in range( sideCount ):
            tur.forward( sideSize )
            tur.right( 180 - angle)

    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur
    ###### Draw here using turtle names tur

