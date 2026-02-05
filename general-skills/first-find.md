## Challenge Information
- **Name:** First Find
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The flag is hidden inside a very large ZIP archive. Extract the files and search for the flag in a file named 'uber-secret.txt'

---

## Approach
When working with a large number of files, manually checking each one is inefficient. The `find` command allows us to quickly locate a specific file across many directories and subdirectories.

---

## Solution Steps
1. Download the challenge file using `wget`.
2. Extract the contents of the ZIP file using `unzip`.
3. Locate the file using the find command: `find . -name "uber-secret.txt"`
- `.` starts the search from the current directory
- `-name` searches for an exact filename
- `-iname` can be used to ignore capitalization
4. Change directory to the file’s location.
5. Display the contents of the file to retrieve the flag: `cat uber-secret.txt`
