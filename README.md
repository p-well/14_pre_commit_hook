# Quadratic Equations Solver

This is script for quadratic equations solving with automatic code testing.<br />
Tests are initiated when user tries to commit changes in repository. Failed tests lead to rejected commit. <br />
The commit is enable when only all tests of ```quadratic_equation.py``` are passed.

Pavel Kadantsev, 2017. <br/>
p.a.kadantsev@gmail.com

# Installation and Usage

Simply clone this repository on your local machine using ```git clone https://github.com/p-well/14_pre_commit_hook.git```.<br />

The following files are stored in repository:

 - quadratic_equation.py - Quadratic equations solver
 - tests.py - Scripts for quadratic_equation.py testing
 - pre-commit - file for running autotests, initialized every time when trying to commit changed in repo.

Copy file ```pre-commit``` into directory ```\.git\hooks``` and try to run commit.

# Example of Script Running

Example of successful tests and commit:

<pre>
<b>>git commit -m "3rd test commit"</b>
....
----------------------------------------------------------------------
Ran 4 tests in 0.000s
</pre>

Example of failed tests and rejected commit:

<pre>
<b>>git commit -m "4th test commit"</b>
F..F
======================================================================
FAIL: test_first_root_less_than_second (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 13, in test_first_root_less_than_second
    self.assertEqual(root1, -3)
AssertionError: -1.0 != -3

======================================================================
FAIL: test_solves_real_roots (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 9, in test_solves_real_roots
    self.assertEqual(root1, 1)
AssertionError: -1.0 != 1

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (failures=2)
</pre>

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
