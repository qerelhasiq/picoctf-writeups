## Challenge Information
- **Name:** Ph4nt0m 1ntrud3r
- **Author:** Prince Niyonshuti N.
- **Category:** Forensics
- **Difficulty:** Easy

---

## Problem Description

A PCAP file is provided for analysis.
The objective is to investigate the network traffic, identify any suspicious activity, and reconstruct the hidden flag embedded within the captured packets.

---

## Approach

The PCAP file is analyzed using Wireshark.
Since the attacker’s actions are embedded within network traffic, the goal is to inspect streams, identify encoded data, and reconstruct the flag from fragmented pieces.

---

## Solution Steps
1. Download the PCAP file
2. Open the file in Wireshark.
3. Adjust the packet order: Sort packets by Time in ascending order to ensure proper sequence of events.
4. Inspect TCP traffic: Identify relevant packets and use `Follow → TCP Stream`
5. Observe encoded data: A Base64-encoded string is found within the stream around time -0.000232.
6. Decode the string: `echo "<base64_string>" | base64 -d`
7. This reveals a portion of the flag.
8. Repeat the process: Continue inspecting subsequent TCP streams.
9. Extract and decode additional Base64 fragments.
10. Reconstruct the flag: Combine all decoded parts in the correct order to obtain the full flag.
