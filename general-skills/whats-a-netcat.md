## Challenge Information
- **Name:** what's a netcat?
- **Author:** Sanjay C/Danny Tunitis
- **Category:** General Skills
- **Difficulty:** Easy

---

## Problem Description
Netcat (`nc`) is a fundamental networking tool that allows direct communication with remote services. In this challenge, a service is running on a remote server and is waiting for incoming connections.
The task is to connect to **fickle-tempest.picoctf.net** on port **52264** using `netcat` and retrieve the flag provided by the service.

---

## Approach
Since the challenge hints at using netcat, the solution is to connect to the given server using the correct nc command format: `nc <server-address> <port-number>`
Running this command establishes a TCP connection and displays the output sent by the server, which includes the flag.

---

## Solution Steps
1. Open a terminal (like Kali Linux).
2. Connect to the remote server using netcat: `nc fickle-tempest.picoctf.net 52264`
3. Once connected, the server responds with the flag.
