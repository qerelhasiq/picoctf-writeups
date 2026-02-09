## Challenge Information
- **Name:** First Grep
- **Author:** Alex Fulton/Danny Tunitis
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Find the flag in the file? Manually scrolling through it would be extremely tedious, so a more efficient method is needed. The flag is hidden somewhere inside the file.

---

## Approach
Since the file contains a large amount of text, manually reading it is inefficient. Instead, command-line tools like `strings` and `grep` can be used to extract readable text and search for patterns that match the flag format.

---

## Solution Steps
1. Download the file using `wget`.
2. Attempt to view the file using `cat`, which reveals a very long and messy output.
3. Use `strings` to extract readable text, then pipe it into `grep` to search for the flag pattern: `strings file | grep "picoCTF{"`
4. This narrows down the search but may still include extra text.
5. Refine the search using a regular expression to extract only the flag: `strings file | grep -o 'picoCTF{[^}]*}'`
- `-o` outputs only the matching part
- `[^}]*` matches everything inside the braces until `}`
