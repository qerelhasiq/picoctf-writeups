## Challenge Information
- **Name:** Rust fixme 1
- **Author:** Taylor McCampbell
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge gives a Rust program that should print a flag, but it has small syntax mistakes that stop it from running. The goal is to fix the errors so the program compiles and prints the flag. It’s a beginner-friendly way to learn some basic Rust stuff like ending statements, returning from a function, and printing variables.

---

## Approach
1. Look at the code and figure out what’s stopping it from running.
2. Check that every line ends correctly with a semicolon (`;`).
3. Make sure the return works correctly if the decryption object fails.
4. Use the correct syntax to print variables with `println!`.
5. Run the program to see the flag.

---

## Solution Steps
1. Add semicolons at the end of statements that need them.
2. Make sure the `if res.is_err()` block returns properly using `return;`.
3. Use `println!("{}", variable)` to print the decrypted flag.
4. Convert the hex values into bytes with `from_str_radix`.
5. Create the XOR decryption object and decrypt the bytes.
6. Run the program (`cargo run`) and read the flag.
