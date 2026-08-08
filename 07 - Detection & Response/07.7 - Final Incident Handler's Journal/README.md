# Healthcare Clinic Ransomware Incident – Incident Handler's Journal

## Overview

This project documents incident response observations and journal entries developed while analyzing cybersecurity incident scenarios. The Incident Handler's Journal provides a structured record for documenting what happened, who was involved, when and where an incident occurred, why it occurred, and any additional observations that may support investigation and response activities.

The first entry documents a ransomware incident affecting a small U.S. healthcare clinic. The incident involved targeted phishing emails, a malicious attachment, ransomware deployment, encryption of critical files, and disruption to access to patient records.

---

## Scenario

A small U.S. healthcare clinic experienced a security incident on a Tuesday morning at approximately 9:00 a.m. Several employees were unable to access files such as medical records, which caused normal business operations to shut down.

Employees also received ransom notes stating that the organization's files had been encrypted by an organized group of unethical hackers. The attackers demanded payment in exchange for the decryption key.

The initial access was gained through targeted phishing emails sent to several employees. The emails contained a malicious attachment that installed malware when downloaded. The attackers then deployed ransomware, which encrypted critical files and prevented employees from accessing important patient information.

---

## Objective

The objective of this journal is to maintain structured documentation of security incidents and record observations that may support investigation, containment, recovery, and future security improvements.

---

# Journal Entry #1

**Date:** 07 August 2026

**Entry Number:** 001

## Description

A small U.S.-based health care clinic experienced a security incident. Employees were unable to access their files, and a ransom note was displayed on their computers, demanding money for the decryption key. To regain access to the organization files, the attackers demanded money in exchange for the decryption key.

Attackers gained unauthorized access by sending phishing emails to the employees. Once the email was clicked, a malicious attachment was downloaded, which installed ransomware and spread across the organization. Employees were unable to access patients' records, which caused major disruption to business operations.

## Tools Used

No cybersecurity tools were used in this activity. N/A.

---

# The 5 W's of the Incident

### Who caused the incident?

An organized group of unethical hackers, who are known for targeting organizations in the healthcare and transportation industries.

### What happened?

Employees were unable to access their files and were displayed a ransom note demanding money for the decryption key.

### When did it happen?

The security incident happened on Tuesday morning at approximately 9:00 AM.

### Where did it occur?

A small U.S. health care clinic specialized in delivering primary-care services.

### Why did it occur?

Several employees in the organization received phishing emails, and one of them downloaded the attachment. Ransomware was deployed on the computers and spread across the company.

---

# Additional Notes

- Employees were unable to identify whether the email was suspicious or a legitimate business email.
- The organization needs to conduct phishing awareness training.
- The organization should maintain regular backups to help recover encrypted files during a ransomware attack.
- The organization should regularly update and patch its systems to reduce security vulnerabilities.

---
# Journal Entry #2 — Wireshark Packet Analysis

**Date:** 07 August 2026

**Entry Number:** 002

## Description

My organization wants to analyze a packet capture file. The captured network traffic was provided as a packet capture file and opened in Wireshark through its Graphical User Interface (GUI). Wireshark provides a practical way to analyze network traffic and examine individual packets in detail.

My objectives for this activity include learning how to navigate through Wireshark, apply display filters, analyze network traffic, inspect individual packets, and understand the information contained within them.

## Tools Used

**Wireshark** — Network protocol analyzer used to inspect and analyze packet capture data.

## Activity Details

### What I Worked On

I used Wireshark to open and analyze a packet capture file. I explored the Wireshark interface, applied display filters to isolate relevant traffic, and inspected individual packets and their protocol information.

### What I Learned

I learned how to navigate through Wireshark, filter traffic using IP addresses and ports, inspect source and destination communication, and analyze protocols such as DNS and HTTP.

I also learned how to examine individual packet details across different protocol layers to better understand how network communication occurs.

### Why It Was Useful

Working with Wireshark helped me understand how packet capture data can be analyzed through a graphical interface. The ability to filter and inspect network traffic can help identify relevant communications and support deeper network investigations.

## Additional Notes

- Wireshark provides a graphical interface for analyzing packet capture data.
- It provides detailed information about individual network packets.
- Display filters make it easier to isolate relevant network traffic.
- Packet details can be examined across multiple protocol layers.
- DNS, TCP, and HTTP traffic can be isolated and analyzed using appropriate filters.
- Learning to analyze packet captures provides a foundation for future network security investigations.

---

# Summary

The Incident Handler's Journal provides a structured record of security incidents, technical investigations, and observations throughout my cybersecurity learning.

The first entry documents a ransomware incident in a healthcare environment. The second and third entries document my practical experience analyzing network traffic using Wireshark and TCPDump, respectively.

Together, these entries show my progression from documenting a security incident to developing practical skills for inspecting and analyzing network traffic using both graphical and command-line tools.


# Journal Entry #3 — TCPDump Packet Capture

**Date:** 08 August 2026

**Entry Number:** 003

## Description

My organization needs to capture and analyze network traffic from a Linux environment. In this activity, I used TCPDump from the command line to identify available network interfaces, inspect live traffic, capture HTTP traffic, and save the captured packets to a PCAP file.

I then reviewed the saved `capture.pcap` file using TCPDump and examined packet information such as IP addresses, ports, TCP flags, sequence numbers, and packet contents. I also used hexadecimal and ASCII output to inspect data carried within the captured packets.

## Tools Used

**TCPDump** — Command-line packet capture and network traffic analysis tool.

**Linux Command Line** — Used to identify network interfaces, capture traffic, and analyze the saved packet capture.

## Activity Details

### What I Worked On

I used TCPDump in a Linux environment to capture and analyze network traffic from the `eth0` interface.

### What I Learned

I learned how to identify available network interfaces, capture live packets, save network traffic to a PCAP file, read previously captured packets, and inspect packet contents using hexadecimal and ASCII output.

### Why It Was Useful

Working with TCPDump helped me understand how network traffic can be observed and analyzed from the command line. This provides a foundation for investigating network communications during future security investigations.

## Additional Notes

- I used `sudo ifconfig` to review the available network interfaces.
- I used `sudo tcpdump -D` to identify interfaces available for packet capture.
- I used `eth0` to capture live network traffic.
- I limited one live capture to five packets to make the output easier to inspect.
- I captured HTTP traffic on port 80 and saved it to `capture.pcap`.
- I used `tcpdump -r` to read the saved packet capture instead of capturing new traffic.
- I used the `-X` option to inspect packet data in hexadecimal and ASCII formats.
- Reviewing saved packet captures provides a useful way to investigate network traffic after the original capture has been completed.