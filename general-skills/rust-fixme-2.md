## Challenge Information
- **Name:** Rust fixme 2
- **Author:** Taylor McCampbell
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
This challenge gives you another Rust program that is supposed to decrypt a hidden flag, but it has some things thats need to be fixed. The program uses XOR decryption and borrowed values, so there is also a little practice understanding how Rust handles variables and mutable references. The goal is to make the program run and print the flag.

---

## Approach
1. Look at the code and see why it won’t run.
2. Make sure the string from main can actually be changed by the function (use mut and &mut).
3. Check that the hex values get turned into bytes properly.
4. Make sure the XOR decryption object works and is used to decrypt the numbers.
5. Run the program and read the flag.

---

## Solution Steps
1. Make the string in main mutable: let mut party_foul = ...
2. Pass it to decrypt as &mut party_foul so the function can change it.
3. Turn the hex numbers into bytes with from_str_radix.
4. Make the XOR decryption object and decrypt the bytes.
5. Add the decrypted result to the string and print it.
6. Run the program and see the flag show up.
