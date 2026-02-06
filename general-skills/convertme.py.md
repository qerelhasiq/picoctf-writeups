## Challenge Information
- **Name:** convertme.py
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Run the Python script and convert the given number from decimal to binary to get the flag.

---

## Approach
The challenge requires understanding decimal to binary conversion. This can be done by repeatedly dividing the number by 2 and keeping track of the remainders, or by using knowledge of binary place values (128, 64, 32, 16, 8, 4, 2, 1).

---

## Solution Steps
1. Download the Python script: `wget <link-address>`
2. Run the script: `python convertme.py`
3. Observe the decimal number provided by the script.
4. Convert the decimal number to binary:
   1. Find the largest power of 2 less than or equal to the number.
   2. Subtract it and continue with the remainder until it reaches 0.
   3. Write 1 for used bits and 0 for unused bits.
   4. For example, 56 can be represented as 32 + 16 + 8, which results in the binary value 00111000
6. Enter the binary result when prompted.
7. The correct conversion reveals the flag.
