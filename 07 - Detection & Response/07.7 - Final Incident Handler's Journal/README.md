# Incident Handler's Journals

## Journal Entry #1 — Healthcare Clinic Ransomware Incident
This entry documents the initial ransomware incident scenario.

**Related Activity:** [07.1 — Incident Handler's Journal](https://github.com/jothish-blip/cybersecurity-portfolio/blob/main/07%20-%20Detection%20%26%20Response/07.1%20-%20Incident%20Handler's%20Journal/README.md)

| **Date:**<br>Record the date of the journal entry. | **Entry:** 001<br>**Date:** 07 August 2026 |
|---|---|
| **Description** | A small U.S.-based health care clinic experienced a security incident. Employees were unable to access their files, and **a ransom note was displayed on their computers**, demanding money for the decryption key. To regain access to the organization files, they demanded money in exchange for the **decryption key**. Attackers gained unauthorized access by sending phishing emails to the employees. Once the email was clicked, a **malicious attachment** was downloaded, which installed ransomware and spread across the organization. Employees were unable to access patients' records, which caused major disruption to business operations. |
| **Tool(s) Used** | No cybersecurity tools were used in this activity. N/A. |
| **The 5 W's** | **Who caused the incident:**<br>An organized group of unethical hackers, who are known for targeting organizations in the healthcare and transportation industries.<br><br>**What happened:**<br>Employees were unable to access their files and were displayed a ransom note demanding money for the decryption key.<br><br>**When did it happen:**<br>The security incident happened on Tuesday morning at approximately 9:00 AM.<br><br>**Where did it occur:**<br>A small U.S. health care clinic specialized in delivering primary-care services.<br><br>**Why did it occur:**<br>Several employees in the organization received phishing emails, and one of them downloaded the attachment. Ransomware was deployed on the computers and spread across the company. |
| **Additional Notes** | - Employees were unable to identify whether the email was suspicious or a legitimate business email.<br>- The organization needs to conduct phishing awareness training.<br>- The organization should maintain regular backups to help recover encrypted files during a ransomware attack.<br>- The organization should regularly update and patch its systems to reduce security vulnerabilities. |

--- 

## Journal Entry #2 — Wireshark Packet Analysis
**Related Activity:** [07.2 — Wireshark Packet Analysis](https://github.com/jothish-blip/cybersecurity-portfolio/blob/main/07%20-%20Detection%20%26%20Response/07.2%20-%20Wireshark%20Packet%20Analysis/README.md)

| **Date:**<br>Record the date of the journal entry. | **Entry:** 002<br>**Date:** 07 August 2026 |
|---|---|
| **Description** | My organization wants to analyze a packet capture file. The captured network traffic was provided as a packet capture file and opened in Wireshark through its Graphical User Interface (GUI). Wireshark provides a practical way to analyze network traffic and examine individual packets in detail.<br><br>My objectives for this activity include learning how to navigate through Wireshark, apply display filters, analyze network traffic, inspect individual packets, and understand the information contained within them. |
| **Tool(s) Used** | **Wireshark** — Network protocol analyzer used to inspect and analyze packet capture data. |
| **Activity Details** | **What I Worked On:**<br>I used Wireshark to open and analyze a packet capture file. I explored the Wireshark interface, applied display filters to isolate relevant traffic, and inspected individual packets and their protocol information.<br><br>**What I Learned:**<br>I learned how to navigate through Wireshark, filter traffic using IP addresses and ports, inspect source and destination communication, and analyze protocols such as DNS and HTTP.<br><br>I also learned how to examine individual packet details across different protocol layers to better understand how network communication occurs.<br><br>**Why It Was Useful:**<br>Working with Wireshark helped me understand how packet capture data can be analyzed through a graphical interface. The ability to filter and inspect network traffic can help identify relevant communications and support deeper network investigations. |
| **Additional Notes** | - Wireshark provides a graphical interface for analyzing packet capture data.<br>- It provides detailed information about individual network packets.<br>- Display filters make it easier to isolate relevant network traffic.<br>- Packet details can be examined across multiple protocol layers.<br>- DNS, TCP, and HTTP traffic can be isolated and analyzed using appropriate filters.<br>- Learning to analyze packet captures provides a foundation for future network security investigations. |

---
## Journal Entry #3 — TCPDump Packet Capture
**Related Activity:** [07.3 — TCPDump Packet Capture](https://github.com/jothish-blip/cybersecurity-portfolio/blob/main/07%20-%20Detection%20%26%20Response/07.3%20-%20TCPDump%20Packet%20Capture/README.md)

| **Date:**<br>Record the date of the journal entry. | **Entry:** 003<br>**Date:** 08 August 2026 |
|---|---|
| **Description** | My organization needs to capture and analyze network traffic from a Linux environment. In this activity, I used TCPDump from the command line to identify available network interfaces, inspect live traffic, capture HTTP traffic, and save the captured packets to a PCAP file.<br><br>I then reviewed the saved `capture.pcap` file using TCPDump and examined packet information such as IP addresses, ports, TCP flags, sequence numbers, and packet contents. I also used hexadecimal and ASCII output to inspect data carried within the captured packets. |
| **Tool(s) Used** | **TCPDump** — Command-line packet capture and network traffic analysis tool.<br><br>**Linux Command Line** — Used to identify network interfaces, capture traffic, and analyze the saved packet capture. |
| **Activity Details** | **What I Worked On:**<br>I used TCPDump in a Linux environment to capture and analyze network traffic from the `eth0` interface.<br><br>**What I Learned:**<br>I learned how to identify available network interfaces, capture live packets, save network traffic to a PCAP file, read previously captured packets, and inspect packet contents using hexadecimal and ASCII output.<br><br>**Why It Was Useful:**<br>Working with TCPDump helped me understand how network traffic can be observed and analyzed from the command line. This provides a foundation for investigating network communications during future security investigations. |
| **Additional Notes** | - I used `sudo ifconfig` to review the available network interfaces.<br>- I used `sudo tcpdump -D` to identify interfaces available for packet capture.<br>- I used `eth0` to capture live network traffic.<br>- I limited one live capture to five packets to make the output easier to inspect.<br>- I captured HTTP traffic on port 80 and saved it to `capture.pcap`.<br>- I used `tcpdump -r` to read the saved packet capture instead of capturing new traffic.<br>- I used the `-X` option to inspect packet data in hexadecimal and ASCII formats.<br>- Reviewing saved packet captures provides a useful way to investigate network traffic after the original capture has been completed. |

---

## Journal Entry #4 — Suspicious File Investigation
**Related Activity:** [07.4 — Investigate a Suspicious File](https://github.com/jothish-blip/cybersecurity-portfolio/blob/main/07%20-%20Detection%20%26%20Response/07.4%20-%20Suspicious%20File%20Investigation/README.md)

| **Date:**<br>Record the date of the journal entry. | **Entry:** 004<br>**Date:** 10 August 2026 |
|---|---|
| **Description** | I am a Cybersecurity analyst working on financial company services. I received an alert about a malicious file being downloaded on an employee's computer. The employee received an email containing a password-protected attachment, and the password was provided in the email. When the password was entered, the file started executing.<br><br>As part of my job, I investigated the file. To start my investigation, I created a SHA256 hash of the file, which cannot be decrypted back into the original file. To further investigate the file and locate the Indicator of Compromise associated with the file, I used VirusTotal, one of the global cybersecurity tools. |
| **Tool(s) Used** | **Linux** — Used to create a SHA256 hash of the file.<br><br>**VirusTotal** — Used to uncover additional Indicators of Compromise. |
| **The 5 W's** | **Who caused the incident:**<br>Unknown malicious actor.<br><br>**What happened:**<br>An unknown malicious actor sent an email containing an attachment protected with a password. The employee used the credentials to open the attachment, and a suspicious file was downloaded onto the computer.<br><br>**When did the incident occur:**<br>At approximately **1:20 PM**, an intrusion detection system found a suspicious file being downloaded and sent an alert.<br><br>**Where did the incident happen:**<br>On an employee's workstation in a financial services company.<br><br>**Why did the incident happen:**<br>The employee received a phishing email containing a password-protected malicious attachment. The employee opened the attachment, and the suspicious file was downloaded. |
| **Additional Notes** | 1. Employees were not able to identify whether files received through email were malicious or legitimate.<br><br>2. The file was associated with multiple domains and IP addresses, which is strong evidence of compromise.<br><br>3. Emails and messages should be verified to determine whether they are legitimate or malicious before opening or clicking them. |

---

## Journal Entry #5 — Phishing Alert Investigation
**Related Activity:** [07.5 — Playbook to respond to a phishing incident](https://github.com/jothish-blip/cybersecurity-portfolio/blob/main/07%20-%20Detection%20%26%20Response/07.5%20-%20Playbook%20to%20respond%20to%20a%20phishing%20incident/README.md)

| **Date:**<br>Record the date of the journal entry. | **Entry:** 005<br>**Date:** 10 August 2026 |
|---|---|
| **Description** | I am a security analyst working at a financial services company. I received an alert about a suspicious file being downloaded on an employee's computer. The file hash was already verified as malicious and reported by several vendors on VirusTotal. As part of the organization's procedure, I need to follow the phishing playbook to conduct further investigation. |
| **Tool(s) Used** | **VirusTotal** — Used to verify the malicious file hash and investigate additional information about the file.<br><br>**Phishing Playbook** — Used as a guide for the step-by-step investigation and response process. |
| **The 5 W's** | **Who caused the incident:**<br>Unknown malicious actor.<br><br>**What happened:**<br>An employee received a phishing email containing a password-protected malicious attachment named `bfsvc.exe`. The password was provided in the email, allowing the employee to open the attachment and download the malicious file onto the computer.<br><br>**When did the incident occur:**<br>The employee received the phishing email on Wednesday, July 20, 2022, at approximately 09:30:14 AM.<br><br>**Where did the incident happen:**<br>On an employee's workstation at a financial services company.<br><br>**Why did the incident happen:**<br>An unknown malicious actor sent a phishing email containing a password-protected malicious attachment. The employee opened the attachment without verifying the email, which allowed the malicious file to be downloaded onto the computer. |
| **Additional Notes** | 1. Employees aren't aware of the phishing emails.<br><br>2. I found that the email is malicious and reported by several vendors.<br><br>3. The email severity is Medium, and the incident has been escalated and sent for further investigation. |

--- 