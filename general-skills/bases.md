## Challenge Information
- **Name:** Bases
- **Author:** Sanjay C/Danny T
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
What does _"bDNhcm5fdGgzX3IwcDM1"_ mean? The hint suggests that it has something to do with bases.

---

## Approach
The given string appears to be encoded rather than encrypted. Its format strongly resembles Base64, which is commonly used to encode text into an ASCII-safe format. To reveal the original message, the string can be decoded using Base64 tools available in Kali Linux.

---

## Solution Steps
1. Decode the string using the Base64 decoder: `echo bDNhcm5fdGgzX3IwcDM1 | base64 -d`
2. The decoded output reveals the hidden message.
3. Wrap the decoded string in the PicoCTF flag format: `picoCTF{<decoded_string>}`
