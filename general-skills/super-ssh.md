## Challenge Information
- **Name:** Super SSH
- **Author:** Jeffery John
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge introduces Secure Shell (SSH). The task is to connect to a remote server using SSH with the given username, host, port, and password. Once logged in successfully, the flag is shown.

---

## Approach
1. Use the `ssh` command with the correct username, server address, and port.
2. Enter the provided password when prompted.
3. Accept the fingerprint if asked.
4. After logging in, the flag should appear.

---

## Solution Steps
1. Open Kali Linux
2. Run the SSH command with the given details:
`ssh ctf-player@titan.picoctf.net -p 60405`
3. Type `yes` when asked to accept the fingerprint.
4. Enter the password: `f3b61b38`.
5. Once logged in, the flag is displayed on the screen.
