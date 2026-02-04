## Challenge Information
- **Name:** repetitions
- **Author:** Theoneste Byagutangaza
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge provides a file named enc_flag containing a string that has been encoded using Base64 multiple times. The objective is to repeatedly decode the content until the original flag is revealed.

---

## Approach
Since the file is Base64-encoded multiple times, the solution is to repeatedly decode the output using the `base64 -d` command until the flag is revealed.

---

## Solution Steps
### Method 1: Manual Repetitive Decryption
1. Display the contents of the encrypted file: `cat enc_flag`
2. Decode the Base64 string using: `echo "<string>" | base64 -d`
3. Take the decoded output and repeat the Base64 decoding process.
4. Continue decoding until the output is readable and reveals the flag.

### Method 2: Automated Decryption
1. Simply run the code:
`data=$(cat enc_flag)
while echo "$data" | base64 -d &>/dev/null; do
  data=$(echo "$data" | base64 -d)
done<
echo "$data"`
2. Flag will be shown
