## Challenge Information
- **Name:** Log Hunt
- **Author:** Yahaya Meddy
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The server logs contain multiple fragments of a secret flag. These fragments are scattered throughout the logs and some of them appear more than once. The task is to analyze the logs and reconstruct the full flag from the pieces provided.

---

## Approach
Analyse the server.log and then use a search function to get the flag

---

## Solution Steps
1. Download the server.log using wget
2. See the contents of server.log using cat
3. Use grep to find the flagpart
4. Combine the flagparts into one flag
