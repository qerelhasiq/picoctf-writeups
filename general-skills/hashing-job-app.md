## Challenge Information
- **Name:** Hashing Job App
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
A set of strings will be given and it must be converted into an MD5 hash.

---

## Approach
MD5 hashing converts input text into a fixed-length hash. Tools like CyberChef make it easy to generate MD5 hashes interactively.

---

## Solution Steps
1. Connect to the challenge server: `nc saturn.picoctf.net 51497`
2. Copy the string provided by the server.
3. Open CyberChef in a web browser: `https://toolbox.itsec.tamu.edu/`
4. Paste the string into the _"Input"_ section.
5. In _"Operations"_, search for MD5 and drag it into the _"Recipe"_ panel.
6. The hashed output will appear under _"Output"_.
7. Enter the MD5 hash back to the server to proceed.
8. Repeat for each string until the flag is shown.
