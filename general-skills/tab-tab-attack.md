## Challenge Information
- **Name:** Tab Tab Attack
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge demonstrates the usefulness of tab completion in the terminal when navigating deeply nested directories and long filenames.---

## Approach
Instead of manually typing long directory and file names, tab completion can be used to automatically complete paths. By repeatedly pressing the **Tab** key, the correct directories can be navigated efficiently. Once the final file is located, its contents can be examined to extract the flag.

---

## Solution Steps
1. Download the challenge file: `wget <challenge-file-url>`
2. Extract the archive: `unzip <filename>.zip`
3. Begin navigating the directories by typing: `cd <first-few-characters>`
   - then repeatedly press Tab until the directory name is completed, and press Enter.
5. Repeat tab completion until reaching the final directory.
6. List the contents: `ls`
7. View the file: `cat <filename>`
8. The output appears as unreadable or binary data.
9. Extract the flag from the file: `strings <filename> | grep "picoCTF{"` OR just manually read the file
