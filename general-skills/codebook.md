## Challenge Information
- **Name:** Codebook
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The challenge provides a Python script (code.py) and a text file (codebook.txt). The script reads from codebook.txt to decode and print the flag. Both files must be located in the same directory for the script to run correctly.

---

## Approach
Since the challenge instructions explicitly state to run the Python script in the same directory as codebook.txt, the solution is simply to download both files into one folder and execute the script.

---

## Solution Steps
1. Create a new directory: `mkdir codebook`
2. Move to the new directory: `cd codebook`
3. Download the required files: `wget <code.py URL>` & `wget <codebook.txt URL>`
4. Run the Python script: `python code.py`
5. The script processes codebook.txt and prints the flag to the terminal.
