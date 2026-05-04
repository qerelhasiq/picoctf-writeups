## Challenge Information
- **Name:** Corrupted File
- **Author:** Yahaya Meddy
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

A corrupted file is provided for analysis. The objective is to determine its intended file type, repair the corruption, and recover the hidden flag.

---

## Approach

The file initially appears as generic data, indicating that its header has been altered.
By examining the first few bytes, it becomes clear that the file contains the JFIF signature, which identifies it as a JPEG image.
However, the standard JPEG magic bytes (FF D8) have been replaced with the ASCII characters \x.
Restoring the correct header repairs the file, allowing it to be opened and analyzed normally.

---

## Solution Steps
1. Download the challenge file: `wget <file-url>`
2. Inspect the file type: `file file`
3. The output identifies it only as generic data, suggesting that the file header is corrupted.
4. Examine the first 16 bytes of the file: `xxd -l 16 file`
  - xxd creates a hexadecimal dump of the file.
  - -l 16 limits the output to the first 16 bytes.
5. Observe the header: `00000000: 5c78 ffe0 0010 4a46 4946 0001 0100 0001`
6. The string JFIF indicates that the file is intended to be a JPEG image.
7. Compare the corrupted and valid JPEG headers:
  - Corrupted: 5C 78 FF E0 ... JFIF
  - Valid:     FF D8 FF E0 ... JFIF
8. Repair the corrupted header: `printf '\xFF\xD8' | dd of=file bs=1 count=2 conv=notrunc`
9. Explanation:
  - printf '\xFF\xD8' outputs the two correct JPEG header bytes.
  - dd writes raw bytes directly to the file.
  - of=file specifies the output file.
  - bs=1 writes one byte at a time.
  - count=2 replaces exactly two bytes.
  - conv=notrunc prevents the file from being truncated after writing.
  - This overwrites the incorrect bytes 5C 78 (ASCII \\x) with the correct JPEG magic bytes FF D8.
10. Verify the repaired file: `file file`
11. The output should now identify the file as a JPEG image.
12. Open the repaired image: `eog file`
13. Extract the embedded text using OCR: `tesseract file output`
14. Display the extracted text: `cat output.txt`
15. Cross-check the OCR output with the image to ensure the flag is captured accurately.
