## Challenge Information
- **Name:** Binary Search
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Figuring out what number has been chosen from 1 to 1000, and you only have 10 guesses to find it. The challenge is to use a strategy to find the correct number efficiently.

---

## Approach
Always take half of the remaining choices for each guess. By guessing the middle number, you can eliminate one half of the possibilities every time. This way, you’re guaranteed to find the correct number within 10 guesses.

---

## Solution Steps
1. Guess 500.  
2. If the number is higher, guess 750. If lower, guess 250.  
3. Continue by adding or subtracting half of the remaining range to your previous guess.  
4. Repeat until you find the correct number.
