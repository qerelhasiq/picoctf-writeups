## Challenge Information
- **Name:** Time Machine
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Sometimes people accidentally leave secrets like passwords or API keys in Git commit messages. These can be easy to miss if you only look at the source code. The goal is to inspect a Git repository’s history and metadata to find anything sensitive that might have been committed by accident.

---

## Approach
1. Look at the commit history to see if any messages contain secrets.
2. Use Git commands to inspect both the messages and the actual changes in commits.
3. Remember that secrets can hide in the metadata, not just the files themselves.  

---

## Solution Steps
1. Run `git log --oneline` to quickly see the list of commits.  
2. Run `git log -p` to view each commit along with the changes it introduced.  
3. Use `git show <commit-hash>` on any suspicious commit to see its full details, including the commit message.  
4. Check for anything that looks like a secret (passwords, API keys, flags, etc.).  
5. Make a note of lessons learned:  
   - People accidentally leave secrets in commit messages.  
   - Auditors should inspect Git metadata, not just source files.  
