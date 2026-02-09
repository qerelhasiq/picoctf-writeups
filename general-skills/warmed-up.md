## Challenge Information
- **Name:** Warmed Up
- **Author:** Sanjay C/Danny Tunitis
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Convert the hexadecimal number 0x3D (base 16) into decimal (base 10).

---

## Approach
Understand how to convert a hexadecimal number to decimal by evaluating each digit’s positional value.

---

## Solution Steps
1. Identify each hex digit:
- 3 in hex = 3 in decimal
- D in hex = 13 in decimal
2. Multiply each digit by its positional power of 16:
- 3 × 16¹ = 48
- 13 × 16⁰ = 13
3. Add them together: `48 + 13 = 61`
4. Format the answer as a flag: `picoCTF{61}`
