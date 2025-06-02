# Network Capture And Analysis ( Task-5 )

---
## Objective
Use Wireshark to capture live network packets and identify fundamental protocols and types of network traffic.

---
## Tools & Environment 
- **Tool used - Wireshark** (Wireshark is a free and open-source network protocol analyzer used for network troubleshooting, analysis, and communication protocol development. It captures and interactively displays the data traveling back and forth on a network in real time.)
- **Platform** - Any system like:-
  - Windows
  - Linux
  - Mac

---
## Installation

- ** For Linux Machine **
  1. Using command prompt
     ```bash
     sudo apt update
     sudo apt install wireshark -y
     ```
  2. To run it using terminal
     ```bash
     wireshark &
     ```
- ** For Windows
  1. Install using
     ```bash
     https://www.wireshark.org/
     ```
  2. Run the installer
     - Double click on .exe file to run it
     - Proceed to utilization by **YES TO ALLOW**
  3. Install **Npcap** or **WinPcap** which is used for capturing live network traffic.

---
## Procedure

1. Start Live capture (after choosing the active Network interface i.e. Ethernet, Wi-Fi from list).
2. Generate traffic by browsing various websites using ping command.
   Example:-
   ```bash
   www.google.com
   www.youtube.com
   www.amazon.in
   ```
   You can also verify that packets are being delivered by running the following command in the Command Prompt
   ```bash
   ping www.youtube.com
   ```
3. Stop the capture after a minute using red square icon.
4. Filter Capture packets using various protocols like http, tcp, icmp.
5. Note source or destination IPs. ports and protocol names (and study protocol-level data).
6. Go to files and save the file as .pcap extension
   ```bash
   test_capture.pcap
   ```
7. Prepare a summary of the recorded session based on the observed network traffic behavior.

---
## Deliverables
- Short Summary
- Capture Files
- Related screenshots

---
## Protocols Identified in Capture

| Protocol    | Description                                 | Observation in Capture                                  |
|-------------|---------------------------------------------|---------------------------------------------------------|
| **DNS**     | Domain Name System, resolves hostnames      | Queries made to resolve domains like `google.com`       |
| **ARP**     | Address Resolution Protocol                 | ARP requests to resolve local IPs on the network        |
| **TCP**     | Transmission Control Protocol               | Connection setup with remote servers                    |
| **TLSv1.2** | Encrypted communication over HTTPS          | Secure sessions with Google and W3Schools               |
| **ICMPv6**  | Internet Control Message Protocol (IPv6)    | Multicast and echo request traffic from system          |

---
## Summary

- DNS queries were observed resolving the domain names of visited websites.

- TCP traffic managed the three-way handshakes and maintained connections to remote servers.

- TLS v1.2/1.3 encryption indicated secure HTTPS sessions during website browsing.

- ARP packets show local network MAC-to-IP resolution activity.

- ICMP or ICMPv6 traffic suggests that IPv4/IPv6 was in use for system-level diagnostics or pings.

- Overall, the capture reflects standard and healthy network communication behavior for secure web browsing.


---
## Outcome
- Developed hands-on skills in using Wireshark.

- Understood how to capture, filter, and analyze packet data.

- Gained insight into common networking protocols and traffic flows.
