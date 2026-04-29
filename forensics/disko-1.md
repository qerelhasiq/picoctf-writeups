## Challenge Information
- **Name:** DISKO 1
- **Author:** Darkraicg492
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

A disk image is provided for analysis. The objective is to examine the image and recover the hidden flag.

---

## Approach

The provided file is a compressed disk image. After decompressing it, the most efficient approach is to search the raw image for printable strings.
Since PicoCTF flags are typically stored in plain text, the strings utility can quickly extract readable content from the disk image.
Filtering the output for the flag format reveals the answer immediately.

---

## Solution Steps
1. Download the compressed disk image: `wget <link-url>`
2. Verify the file type: `file disko-1.dd.gz`
3. Decompress the disk image: `gunzip disko-1.dd.gz`
4. Confirm the extracted file is a disk image: `file disko-1.dd`
5. Extract printable strings from the disk image and search for the flag: `strings disko-1.dd | grep "picoCTF"`
6. The command returns the flag directly.
