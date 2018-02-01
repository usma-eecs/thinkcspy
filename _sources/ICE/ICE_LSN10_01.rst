..  Copyright (C) Tom Babbitt, Kyle King, and Chip Schooler.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Debugging and Use of Libraries
==========================================================

Overview
--------------

In this ICE, we are going to review debugging. We will do that through tracing the codes using *codelens* and through testing. 

#. Click Run and then *codelens* to trace the program

#. What are the expect values? How can we test?
   

Tracing and Debugging
---------------------
What is the expected outcomes of the two function? How can we debug?

**Modifications:** Modify the function(s) so they work properly.

.. activecode:: ICE_LSN10_01
    :nocanvas:

    ### Function to change Celsius to Fahrenheit.   
    def ctof(c):
     return 9/5 * c + 32

    ### Function to change Fahrenheit to Celsius. 
    def ftoc(f):
     return 5/9 * f - 32

    #Change 0C to F 
    tempC = 0
    FTemp = ctof(tempC)
    print("tempC = 0 changed to FTemp = " + str(FTemp))

    #Change 32F to C
    tempF = 32
    CTemp = ftoc(tempF)
    print ("tempF = 32 changed to CTemp = " + str(CTemp))

Test other known values to confirm your updates fixed the problem.

Revisiting Random
-----------------

We used ``random`` in the Algorithm lesson. The ``random`` module has many options. The options can be seen at https://docs.python.org/3/library/random.html.

Let's explore its use:


.. activecode:: ICE_LSN10_02
    :nocanvas:
       
    import random
    x = ['tim','bob','john','mike']
    random.shuffle(x)
    print(x)

    ### Now use random.randint() to randomly
    ### return a number between 1 and 125.

The ``shuffle`` function as called in the example above, randomly orders the values in list *x*. 

    
