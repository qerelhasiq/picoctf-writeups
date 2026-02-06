## Challenge Information
- **Name:** fixme2.py
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Fix the syntax error in the provided Python script to print the flag.

---

## Approach
Identify the syntax error by running the script and analyzing the Python traceback. Python errors often include the line number and type of error, which helps locate the problem quickly.

---

## Solution Steps
1. 1. Download the Python script: `wget <link-address>`
2. Run the script to see the error: `python <python-script>.py`
3. Observe the error message: `SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?`
4. Note the line number where the error occurs: `File "path/directory", line 22`
5. Edit the script to fix the error: `nano <python-script>.py`
6. Change the operator to a comparison (==) because the goal is to check if flag is empty:
- = is assignment, which sets flag to a value. Using it in an if statement causes a SyntaxError.
- == is comparison, which checks whether flag equals the empty string — exactly what we want here.
- := (walrus operator) assigns and evaluates in one step. Using it would assign "" to flag, which is not intended and would make the condition evaluate incorrectly.
8. Run the script again: `python <python-script>.py`
9. The flag is printed.
