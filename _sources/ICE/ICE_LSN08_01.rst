..  Copyright (C) Tom Babbitt, Kyle King, and Chip Schooler.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

The Power of an Algorithm - Comparison of Algorithmic Time
==================================================


Random Numbers
--------------

Before beginning to  write code for this in class exercise, we need to introduce two additional Python modules. The ``random`` module allows us to generate random numbers.
It's easy to use:


.. activecode:: ICE_LSN08_01
    :nocanvas:
       
    import random
    x = random.sample(range(100),10)
    print(x)

The ``sample`` function as called in the example above, generates a list of range numbers in the *range*.
The variable x is a list of 10 numbers in the *range* from 0 to 99. The ``sample`` function does not allow duplicates from
the *range*.

Finding Time
------------
The ``datetime`` module allows us to determine the exact time.    

.. activecode:: ICE_LS08_02
    :nocanvas:
       
    import datetime
    t = datetime.datetime.now()
    print(t)

The ``datetime.now()`` function as called in the example above, returns the current time displayed by the computer. Take note of
how the output to the screen looks.

Comparison of Times
-------------------

In this ICE, we are going to show the power of an algorithm. The better the design the faster it runs on a computer. This
can have huge ramifications. No on likes to wait while the computer processes an application. In fact, many of you have
probably killed an applications that you have to wait on and likely will not use that particular program again.

We will use two different sorting algorithms to show how design can make a difference in time. The first is the python ``sort()``
function associated with a list. The second is a bubble sort algortim all ready written ``bubbleSort(aList)``.

Here is a possible sequence of steps that we will need to accomplish:

#. Import the modules we need

#. Create a list of random numbers

#. Copy the list of random numbers

#. Determine the start time for ``sort()``

#. Run ``sort()`` on a copy of the list

#. Determine the end time for ``sort()`` and print

#. Determine the start time ``bubbleSort(aList)``

#. Run ``bubbleSort(aList)`` on the unsorted copy of the list.

#. Determine the end time for ``bubbleSort()`` and print

#. Find the Difference.

.. activecode:: ICE_LSN08_03
   :nocodelens:

   import random                                           # 1. import modules  
   import datetime 

   def bubbleSort(alist):
      for passnum in range(len(alist)-1,0,-1):
         for i in range(passnum):
            if alist[i]>alist[i+1]:
               temp = alist[i]
               alist[i] = alist[i+1]
               alist[i+1] = temp  


   my_randoms = random.sample(range(1000),1000)          # 2. Creates a list of random numbers
   my_randoms2 = list(my_randoms)                        # 3. Creates a copy of the random list

   a = datetime.datetime.now()                           # 4. Start time for sort()
   my_randoms.sort()                                     # 5. Sort the list using sort()
   b = datetime.datetime.now()                           # 6. End time for sort()
   print(b-a)                                            # 7. Print the difference

   # your code goes here


Take a look at step 4-7 and use the function ``bubbleSort(aList)`` to determine the time it takes. Make sure that you sort **my_randoms2**.

    
