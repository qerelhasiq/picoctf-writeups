## Challenge Information
- **Name:** red
- **Author:** Shuailin Pan (LeConjuror)
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

A PNG image is provided for analysis. The objective is to investigate the file, identify any hidden data, and extract the flag.

---

## Approach

The image appears visually simple, but metadata and steganographic analysis techniques are required to uncover hidden information.

---

## Solution Steps
1. Download the file: `wget <link_to_file>`
2. Visually inspect the image to confirm it appears as a solid red PNG: `eog red.png`
3. Check metadata using ExifTool: `exiftool red.png`
4. A poem is found within the metadata. Taking the first letter of each line forms the keyword: `CHECKLSB`
5. This indicates that LSB (Least Significant Bit) steganography is used.
6. Run zsteg to analyze hidden data in the PNG: `zsteg red.png`
7. The output reveals a Base64-encoded string hidden in the image.
8. Decode the extracted string: `echo "<string>" | base64 -d`
9. The decoded output reveals the flag.
