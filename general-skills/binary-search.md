## Challenge Information
- **Name:** Binary Search
- **Author:** Jeffrey John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The challenge presents a number guessing game where a value between 1 and 1000 is chosen.
The goal is to determine the correct number within **10 guesses**, encouraging the use of an efficient search strategy.

---

## Approach
Since the number range is sorted and limited, **binary search** is the most efficient approach.
By repeatedly guessing the midpoint of the remaining range and adjusting based on feedback (higher or lower), half of the possible values can be eliminated with each guess.

This ensures the correct number can be found within the allowed number of attempts.

---

## Solution Steps
1. Start by guessing the midpoint of the range (500).
2. If the correct number is higher, adjust the range to 501–1000.
3. If the correct number is lower, adjust the range to 1–499.
4. Repeat the process by guessing the midpoint of the new range.
5. Continue narrowing the range until the correct number is identified within 10
