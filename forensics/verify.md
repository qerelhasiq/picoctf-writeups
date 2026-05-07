## Challenge Information
- **Name:** Verify
- **Author:** Jeffery John
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

Multiple encrypted files are provided on a remote system, along with a SHA-256 checksum and a decryption script.
The objective is to identify which file is authentic by verifying its checksum, then decrypt the correct file to recover the flag.

---

## Approach

The challenge revolves around file integrity verification using SHA-256 hashes.
Since several files may contain fake or misleading data, the provided checksum is used to identify the legitimate file.
Once the correct file is verified, the provided decryption script can be used to recover the flag.

---

## Solution Steps
1. Connect to the remote machine using SSH: `ssh -p 57208 ctf-player@rhea.picoctf.net`
2. Accept the SSH fingerprint when prompted.
3. Enter the provided password: `6abf4a82`
4. List the files in the current directory: `ls`
5. The directory contains: checksum.txt, decrypt.sh & files/
6. View the provided checksum: `cat checksum.txt`
7. The SHA-256 checksum acts as a fingerprint for the legitimate file.
8. Generate SHA-256 hashes for all files inside the files directory: `sha256sum files/*`
9. Search for the file whose hash matches the provided checksum: `sha256sum files/* | grep "<checksum>"`
10. Example output: `b09c99... files/real.txt`
11. The matching hash confirms that the file is authentic and has not been altered.
12. Decrypt the verified file using the provided script: `./decrypt.sh files/real.txt`
13. The script outputs the flag.
