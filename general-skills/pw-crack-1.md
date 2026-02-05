## Challenge Information
- **Name:** PW Crack 1
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The goal is to crack the password required to decrypt and reveal the flag. The challenge provides a Python password checker script and an encrypted flag file, which must be placed in the same directory.

---

## Approach
Two files are provided: a Python script and an encrypted flag. Since the encrypted flag cannot be opened directly, the Python script is inspected to understand how the password check works. The password is revealed in plaintext within the script.

---

## Solution Steps
1. Download the Python script and the encrypted flag using `wget`.
2. Ensure both files are in the same directory.
3. Inspect the Python script using a text editor such as nano: `nano <filename>.py`
4. Identify the password, which is stored in plaintext within the script.
5. Run the script: `python <filename>.py`
6. Enter the password obtained from the script.
7. The script successfully decrypts and displays the flag.
