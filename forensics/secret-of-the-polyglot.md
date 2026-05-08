## Challenge Information
- **Name:** Secret of the Polyglot
- **Author:** Lt 'Syreal' Jones
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

The Network Operations Center (NOC) has identified a suspicious file that appears to present conflicting file-type information.
The objective is to analyze the file, determine its true structure, and extract all hidden information contained within it.

---

## Approach

The file exhibits characteristics of multiple file formats.
By inspecting its metadata and actual byte structure, it is possible to determine how different applications interpret different parts of the same file.

---

## Solution Steps
1. Download the file: `wget <file_url>`
2. Open the file as a PDF: `evince flag2of2-final.pdf`
3. This reveals the second part of the flag.
4. Verify the file type using: `file flag2of2-final.pdf`
5. The output indicates that the file also contains PNG data.
6. Confirm this further using metadata inspection: `exiftool flag2of2-final.pdf`
7. Since the file contains embedded image data, rename it to force image interpretation: `mv flag2of2-final.pdf flag2of2-final.png`
8. Open the file as an image: `eog flag2of2-final.png`
9. This reveals the first part of the flag.
10. Combine both parts to get the full flag
