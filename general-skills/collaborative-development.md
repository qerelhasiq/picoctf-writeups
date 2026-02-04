## Challenge Information
- **Name:** Collaborative Development
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The author's team worked hard on new features for their flag printing program. The challenge provides multiple branches in a Git repository, each containing a part of the final flag printing program. The task is to combine these contributions into a single working program to reveal the flag.

---

## Approach
This challenge is designed to simulate a collaborative development scenario. Multiple branches contain partial implementations of the flag.py file. The goals were to:
1. Explore all branches using git branch -a.
2. Inspect the contents of flag.py in each branch.
3. Merge the branches carefully into the main branch, resolving any merge conflicts.
4. Ensure that all flag fragments are combined correctly to print the complete flag.

---

## Solution Steps

### Method 1: Using Git Merge
1. List all branches: `git branch -a`
2. Switch to the main branch (final product): `git checkout main`
3. Merge the first two feature branches: `git merge feature/part-1` & `git merge feature/part-2`
4. If a conflict occurs (as it does with feature/part-2), open the conflicting file: `nano flag.py`
  - Remove the conflict markers (<<<<<<< HEAD, =======, >>>>>>> feature/part-2) and manually combine the flag pieces.
5. Mark the conflict as resolved and commit: `git add flag.py` & `git commit -m "Resolved merge conflict for feature/part-2"`
6. Merge the last branch: `git merge feature/part-3`
7. Resolve any conflicts the same way as before, then `git add flag.py` and `git commit`.
8. Run the final program to reveal the flag: `python3 flag.py`

### Method 2: Manual Combination (Without Merging)
1. List all branches: `git branch -a`
2. Checkout each feature branch individually: `git checkout feature/part-1`, `git checkout feature/part-2`, `git checkout feature/part-3`
3. View the contents of _flag.py_ in each branch: `cat flag.py`
4. Manually combine the flag pieces from each branch into one complete file in the main branch.
5 Run the combined flag.py: `python3 flag.py`
