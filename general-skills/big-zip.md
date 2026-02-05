## Challenge Information
- **Name:** Big Zip
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The flag is hidden inside a very large ZIP archive. Extract the files and search for the flag.

---

## Approach
When working with a large number of files, manually checking each one is inefficient.
The `grep` command allows us to quickly search for specific strings across many files and directories.

---

## Solution Steps
1. Download the challenge file using `wget`.
2. Extract the contents of the ZIP file using `unzip`.
3. Use grep with the recursive option to search for the flag pattern: `grep -R "picoCTF{"`
- The command searches all files and subdirectories and reveals the flag.
