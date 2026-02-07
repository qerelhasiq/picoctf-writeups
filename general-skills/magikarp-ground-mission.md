## Challenge Information
- **Name:** Magikarp Ground Mission
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge tests basic Linux command-line navigation and file reading skills. After connecting to a remote container via SSH, you must move between directories and read files to retrieve parts of the flag.

---

## Approach
The challenge requires connecting to a remote machine via SSH and following instructions found in text files. Each instruction guides you to a different directory using common Linux path shortcuts (/, .., and ~). By navigating correctly and reading the files in each location, all parts of the flag can be collected and combined.

---

## Solution Steps
1. Connect to the target using SSH: `ssh -p 51303 ctf-player@wily-courier.picoctf.net`
2. Type 'yes' when prompted to accept the host fingerprint.
3. Enter the password: `8c606eb1`
4. Check the current directory: `pwd` which gives `/home/ctf-player/drop-in`
5. List the files: `ls`
6. Read the first flag part: `cat 1of3.flag.txt`
7. Read the instructions for the next step: `cat instructions-to-2of3.txt`
8. The instruction says to go to the root directory (/).
9. Move to the root directory: `cd /`
- (Using cd ../../.. also works, but cd / is simpler and clearer.)
10. List the files again: `ls`
11. Read the second flag part: `cat 2of3.flag.txt`
12. Read the next instruction: `cat instructions-to-3of3.txt`
13. It tells you to go “home”, represented by ~.
14. Go to the home directory: `cd ~`
- (~ automatically expands to /home/ctf-player for this user.)
15. List the files: `ls`
16. Read the final flag part: `cat 3of3.flag.txt`
17. Combine all three flag parts in the order you found them to obtain the full flag.
