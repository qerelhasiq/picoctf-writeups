## Challenge Information
- **Name:** Commitment Issues
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The flag was wriitten down, however the author allegedly deleted it.

---

## Approach
1. Download and extract the provided archive
2. Explore the contents of the unzipped folder to locate any files containing hints or the flag
3. Inspect the Git commit history to identify deleted or modified files
4. Restore files from previous commits if necessary to recover the flag

---

## Solution Steps
1. wget the zipped file
2. `unzip <file>` whereby <file> is challenge.zip
3. cd to the unzipped folder
4. `cat message.txt` will say 'TOP SECRET'
5. `git log --oneline` to check the commit history
6. `git checkout ea859bf` to restore a file or commit that was deleted or modified
7. `cat message.txt` will give the flag

---

## Note
If the log says to commit your changes or stash, run this:
1. git stash
2. git stash list
3. git checkout -f <git-commit-hash>
4. ls -la
5. cat message.txt
