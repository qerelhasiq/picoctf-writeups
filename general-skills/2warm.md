## Challenge Information
- **Name:** 2warm
- **Author:** Sanjay C/Danny Tunitis
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Convert the number 42 from base 10 (decimal) to base 2 (binary).

---

## Approach
The challenge requires understanding decimal to binary conversion. This can be done by repeatedly dividing the number by 2 and keeping track of the remainders, or by using knowledge of binary place values (128, 64, 32, 16, 8, 4, 2, 1).

---

## Solution Steps
1. 1. Break 42 into powers of two:
   - 42 = 32 + 8 + 2
2. Map the values to binary place positions:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----|----|----|----|---|---|---|---|
|  0  | 0  | 1  | 0  | 1 | 0 | 1 | 0 |

3. The binary representation of 42 is: 00101010
