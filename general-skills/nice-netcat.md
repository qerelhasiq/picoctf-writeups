## Challenge Information
- **Name:** Nice netcat...
- **Author:** Lt 'Syreal' Jones
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
The challenge provides a service that can be accessed using netcat. When connected, the service outputs a sequence of numbers instead of readable text.

---

## Approach
After connecting to the service with `nc`, the output consists of decimal ASCII values. Converting these numbers to their corresponding ASCII characters reveals the hidden message, which contains the flag. This can be done manually using an ASCII table or automatically using command-line tools.

---

## Solution Steps
1. Connect to the remote service: `nc wily-courier.picoctf.net 55461`
2. The service outputs a list of numbers separated by spaces or new lines. These numbers represent decimal ASCII values.
3. Convert the ASCII values to characters.

### Manual method:
- Use an ASCII table to map each decimal value to its corresponding character.
- For example: https://www.eso.org/~ndelmott/ascii.html

### Automated method:
- nc wily-courier.picoctf.net 55461 | tr ' ' '\n' | awk '{printf "%c", $1}'
- The decoded output reveals the flag.
