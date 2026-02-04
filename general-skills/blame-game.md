## Challenge Information
- **Name:** Blame Game
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Someone's commit seems to be preventing the program from working. The goal is to identify which contributor introduced the breaking change.

---

## Approach
In collaborative Git projects, multiple contributors may modify the same file over time. To identify who introduced a problematic change, Git provides the git blame command. This command shows line-by-line attribution, revealing which user last modified each line of a file. By analyzing the line that caused the error, we can determine the responsible contributor.

---

## Solution Steps
1. Extract the challenge files using: `unzip <zipped-file-name>`
2. Inspect the source code: `cat message.py`
  - The file contains a syntax error, indicating why the program does not run correctly.
3. Use Git blame to identify who last modified the faulty line: `git blame message.py`
  - The output shows the contributor responsible for the line containing the syntax error. This name corresponds to the answer (flag).
