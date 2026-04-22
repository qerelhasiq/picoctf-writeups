## Challenge Information
- **Name:** Hidden In Plainsight
- **Author:** Yahaya Meddy
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description
A JPG image file is provided that appears to be ordinary. However, data has been hidden within the file.
The task is to identify the concealed payload and extract the flag.

---

## Approach
Since the image appears normal, the first step is to analyze its metadata for any hidden clues such as encoded strings, tool references, or passwords.

---

## Solution Steps
1. Download the PDF file:  `wget fileurl`
2. Extract metadata using: `exiftool filename`
3. Inspect the output: A Base64-encoded string is present in the Comment field
4. Decode the string: `echo base64-string | base64 -d`
5. It gives a two-part output: `steghide:cEF6endvcmQ=`. steghide is a tool, and the part after : is another encoded string
6. Decode the string: `echo base64-string | base64 -d` to give the password to use with steghide
7. Extract the hidden data using steganography: `steghide extract -sf filename` -sf specifies the stego file (the file containing hidden data)
8. The extracted data is put into _flag.txt_
9. Read the flag: `cat flag.txt`
