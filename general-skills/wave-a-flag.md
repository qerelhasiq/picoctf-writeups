## Challenge Information
- **Name:** Wave a flag
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
A binary program contains a hidden flag. The program exposes helpful information via its help flag (-h), which can be used to reveal the flag instead of directly inspecting the binary.

---

## Approach
The challenge hints that the binary exposes useful information through its help flag. Instead of inspecting the file contents directly, the intended solution is to execute the program and request its help output, which reveals the flag.

---

## Solution Steps
1. Download the challenge file: `wget <challenge-file-url>`
2. Make the binary executable: `chmod +x <filename>`
3. Invoke the help flag: `./<filename> -h`
4. The flag is displayed directly in the output.


## Note: Why not use grep?

### Static Analysis (grep) vs Dynamic Analysis (-h)

| Approach                | Command       | What it does                                                                                                                      | Pros                                                                                                                                                                | Cons                                                                                     |                                                                                                                                    |
| ----------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Static Analysis**     | `strings warm | grep picoCTF`                                                                                                                     | Scans the binary file directly for readable ASCII strings.<br>Extracts printable text without executing the program.<br>Ignores how the program is intended to run. | Fast<br>Effective in CTFs                                                                | Not always possible in real-world scenarios.<br>May fail on stripped or packed binaries.<br>Requires read permissions on the file. |
| **Dynamic Interaction** | `./warm -h`   | Runs the program as intended.<br>Enumerates exposed functionality via help output.<br>Lets the program reveal information itself. | More realistic.<br>Teaches proper enumeration habits.<br>Reflects common real-world misconfigurations.                                                              | Slightly slower in CTF speedruns.<br>Requires the binary to be executable on the system. |                                                                                                                                    |

### Real‑World Analogy 🔐

- `strings | grep` → You stole the blueprints and found secrets written inside
- `-h` → You walked up to the building and the front desk gave you the password
- Both work — but only one reflects how real security mistakes usually happen.
