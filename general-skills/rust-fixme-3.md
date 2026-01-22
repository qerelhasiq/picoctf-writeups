## Challenge Information
- **Name:** Rust fixme 3
- **Author:** Taylor McCampbell
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The challenge provides a Rust program that is supposed to decrypt a hidden flag, but it contains syntax errors that prevent it from running. The task is to fix the errors, run the code successfully, and print the flag. The program demonstrates some unsafe memory operations in Rust and uses an XOR-based decryption method.

---

## Approach
1. Look at the Rust code and find anything that would stop it from running.
2. Make sure the encrypted numbers and other values have the right types so Rust understands them.
3. Fix the unsafe part so the program can read the decrypted data.
4. Check that the XOR decryption object is created and actually used to decrypt the numbers.
5. Run the program and make sure it prints the flag with the message.

---

## Solution Steps
1. Install Rust (rustc and cargo).
2. Open the provided Rust code.
3. Fix any problems in the code:
    - Make sure the hex numbers are in the right format.
    - Make sure the unsafe block is uncommented so it can read the decrypted data.
4. Run the program using cargo run.
5. Read the output — it will show the flag along with a message.
