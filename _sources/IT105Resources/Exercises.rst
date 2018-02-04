..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Exercise Examples
-----------------
Below is an example of a question that could be asked as part of a problem set or graded lab. Many of the questions will give
feedback. There will be some that due to what is being asked there is no efective way to provide test cases and feedback. Those
questions will be identified through comments when you run your program.

**Programming Problem Set 1** review the exercises in Lists and Functions Chapters.

.. question:: IT105Resoures_ex_1


   .. tabbed:: q1

        .. tab:: Question

           .. actex:: IT105Resoures_ex_1_1q

              Write a function to count how many even numbers are in a list.
              ~~~~
              def countEven(lst):
                  # your code here

              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(countEven([1,3,5,7,9]),0,"Tested countEven on input [1,3,5,7,9]")
                      self.assertEqual(countEven([1,2,3,4,5]),2,"Tested countEven on input [1,2,3,4,5]")
                      self.assertEqual(countEven([2,4,6,8,10]),5,"Tested countEven on input [2,4,6,8,10]")
                      self.assertEqual(countEven([0,-1,12,-33]),2,"Tested countEven on input [0,-1,12,-33]")

              myTests().main()



        .. tab:: Answer

            .. activecode:: IT105Resoures_ex_1_1a

                import random

                def countEven(lst):
                    even = 0
                    for e in lst:
                        if e % 2 == 0:
                            even += 1
                    return even

                # make a random list to test the function
                lst = []
                for i in range(100):
                    lst.append(random.randint(0, 1000))

                print(countEven(lst))

   



