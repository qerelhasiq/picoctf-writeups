## Challenge Information
- **Name:** Glitch Cat
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The flag is displayed, but it is not in the correct format because some parts of it are shown as hexadecimal values. These hex values must be converted to ASCII to obtain the full flag.

---

## Approach
Identify the hexadecimal portions of the flag and convert them into ASCII characters using common command-line tools or scripting methods.

---

## Solution Steps
1. Connect to the challenge server: `nc saturn.picoctf.net 55333`
2. The flag is immediately displayed, but some characters are represented in hexadecimal.
3. Convert the hexadecimal values to ASCII using one of the following methods:

### Method 1: printf
`printf '\x61\x34\x33\x39\x32\x64\x32\x65'`

### Method 2: Python
`python3 -c "print(chr(0x61)+chr(0x34)+chr(0x33)+chr(0x39)+chr(0x32)+chr(0x64)+chr(0x32)+chr(0x65))"`

### Method 3: xxd
`echo "61 34 33 39 32 64 32 65" | xxd -r -p`
- `xxd` creates and reverses hex dumps
- `-r` reverses hex back to binary
- `-p` uses plain hex input without addresses or ASCII columns

4. Combine the decoded ASCII characters with the rest of the flag to obtain the complete flag.
