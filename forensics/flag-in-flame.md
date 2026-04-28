## Challenge Information
- **Name:** Flag in Flame
- **Author:** Prince Niyonshuti N.
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

A suspiciously large log file was discovered following a recent security breach. Upon inspection, it was found to contain a large block of encoded data instead of normal log entries.
The task is to analyze the file, identify any hidden information, and extract the flag concealed within it.

---

## Approach

The file appears to be encoded rather than plain text logs. The investigation begins by decoding the data, identifying the resulting file type, and then analyzing it for hidden or embedded information.

---

## Solution Steps
1. Download the file: `wget <file_url>`
2. Decode the Base64-encoded content into a binary file: `base64 -d logs.txt > file.bin`
3. Identify the file type: `file file.bin`
4. Since the output indicates a PNG image, rename the file accordingly: `mv file.bin file.png`
5. Analyze the image structure: `binwalk file.png` & `pngcheck -v file.png`
6. Open the image to visually inspect it: `eog file.png`
7. A hidden string is observed within the image.
8. Extract embedded text using OCR: `tesseract file.png output`
9. Read the text: `cat output.txt`
10. Decode the extracted hexadecimal string into readable ASCII: `echo "<hex_string>" | xxd -r -p`

Command explanation:
xxd → converts binary/hex data
-r → reverse operation (hex → binary/text)
-p → plain hex format input
