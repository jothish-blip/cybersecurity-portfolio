# 03 – Incident Report Analysis

## Overview

This activity analyzes a network security incident experienced by a fictional multimedia company that provides web design, graphic design, and social media marketing services.

The incident is examined using the **NIST Cybersecurity Framework (NIST CSF)** to understand what happened, identify the security weaknesses that allowed the attack, and recommend improvements that reduce the likelihood of similar incidents in the future.

---

# Incident Summary

The company experienced a **Denial-of-Service (DoS)** attack that disrupted its internal network for approximately **two hours**.

During the incident, a large volume of **ICMP packets** flooded the network, preventing employees from accessing internal resources and causing several network services to become unavailable.

The incident response team immediately blocked incoming ICMP traffic, temporarily shut down non-critical network services, and restored critical business services.

A post-incident investigation revealed that the attacker exploited an **unconfigured firewall**, allowing malicious ICMP traffic to overwhelm the company's internal network.

No evidence of data theft or unauthorized access to sensitive information was found.

---

# Identify

## Type of Attack

- Denial-of-Service (DoS)
- ICMP Flood Attack

## Vulnerability Exploited

- Unconfigured firewall
- Missing traffic filtering rules

## Systems Affected

- Internal network
- Network services
- Employee access to internal resources

## Impact

- Internal network unavailable for approximately two hours
- Employees unable to access network resources
- Business operations temporarily interrupted
- No data breach identified

---

# Protect

To reduce the risk of similar attacks, the following security improvements should be implemented:

- Configure firewall rules to limit excessive ICMP traffic.
- Enable rate limiting for incoming network requests.
- Verify source IP addresses to reduce spoofed traffic.
- Regularly review firewall configurations.
- Deploy Intrusion Detection and Intrusion Prevention Systems (IDS/IPS).
- Provide routine security awareness training for IT staff.

---

# Detect

Improving network visibility will allow future attacks to be identified much earlier.

Recommended detection measures include:

- Deploy a Security Information and Event Management (SIEM) solution.
- Monitor firewall logs continuously.
- Configure IDS/IPS to detect abnormal ICMP traffic.
- Generate alerts for unusual network activity.
- Perform regular reviews of network traffic and security logs.

---

# Respond

If a similar incident occurs in the future, the organization should follow a structured response process.

### Response Actions

- Block malicious network traffic immediately.
- Isolate affected systems if necessary.
- Keep critical business services available whenever possible.
- Collect firewall logs and network evidence for investigation.
- Identify the root cause of the incident.
- Update firewall rules and security controls before restoring normal operations.
- Document the incident and review lessons learned.

---

# Recover

After the attack has been contained, the organization should restore normal business operations.

Recovery activities include:

- Restore all affected network services.
- Verify firewall configurations before reconnecting systems.
- Confirm that no malicious activity remains.
- Monitor the network for recurring attacks.
- Review security controls and update incident response procedures.
- Schedule regular security assessments to reduce future risk.

---

# Key Findings

The investigation identified that the primary cause of the incident was an improperly configured firewall, which allowed a large volume of ICMP traffic to enter the internal network.

Although the attack caused temporary service disruption, there was no indication that customer data or confidential business information was compromised.

The incident also highlighted the importance of proactive monitoring, properly configured security devices, and well-defined incident response procedures.

---

# Recommendations

## Network Security

- Configure firewall rules correctly.
- Apply ICMP rate limiting.
- Enable source IP verification.
- Conduct periodic firewall audits.

## Monitoring

- Deploy IDS and IPS.
- Implement SIEM for centralized monitoring.
- Monitor network traffic continuously.

## Incident Response

- Maintain an updated incident response plan.
- Perform regular security drills.
- Document all security incidents.
- Review lessons learned after every incident.

## Continuous Improvement

- Perform regular vulnerability assessments.
- Keep security devices updated.
- Train employees on security best practices.
- Review network configurations periodically.

---

# Conclusion

The DoS attack demonstrated how a single firewall misconfiguration can significantly disrupt business operations. While the organization successfully restored services within two hours, the incident exposed weaknesses in network protection and monitoring.

By strengthening firewall configurations, improving network monitoring, implementing IDS/IPS solutions, and maintaining a well-defined incident response process, the organization can better protect its infrastructure against future denial-of-service attacks.