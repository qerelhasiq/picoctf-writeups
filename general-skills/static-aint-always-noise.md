## Challenge Information
- **Name:** Static ain't always noise
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge provides a compiled binary and a helper bash script. The goal is to inspect the binary’s contents to locate a hidden flag.

---

## Approach
Since the file is a binary, viewing it directly with `cat` produces unreadable output. The provided bash script automates binary analysis by disassembling the executable and extracting readable strings. By searching these extracted strings, the embedded flag can be easily identified.

---

## Solution Steps
1. Make the helper script executable: `chmod +x ltdis.sh`
2. Run the script on the binary: `./ltdis.sh static`
3. The script generates output files, including a strings dump: `static.ltdis.strings.txt`
4. Search the extracted strings for the flag: manually or `grep "picoCTF{" static.ltdis.strings.txt`
