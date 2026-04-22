## Challenge Information
- **Name:** Riddle Registry
- **Author:** Prince Niyonshuti N.
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description
A PDF document has been provided that appears to contain only garbled and meaningless content. However, this visible data is intentionally misleading. Embedded within the file is a hidden piece of information that is not immediately apparent.

The task is to analyze the provided file, “Hidden Confidential Document,” and uncover the hidden flag located within its metadata.

---

## Approach
Ignore visible data or content, check the metadataThe visible content of the PDF is intentionally misleading. Instead of focusing on what’s displayed, shift attention to the file’s metadata, where the actual clue is hidden.

---

## Solution Steps
1. Download the PDF file:  `wget file`
2. Extract metadata using: `exiftool filename`
3. Inspect the output: A Base64-encoded string is present in the Author field
4. Decode the string to reveal the flag: `echo base64-string | base64 -d`
