# 02 – Conduct an Audit (Controls & Compliance Checklist)

## Overview

This activity demonstrates how to perform an internal security audit for **Botium Toys**, a fictional U.S.-based toy company that is expanding its online business. As the company grows, its IT infrastructure and security requirements become more complex.

The audit follows the **NIST Cybersecurity Framework (NIST CSF)** to evaluate the organization's current security posture. The objective is to identify existing security controls, determine compliance gaps, assess organizational risks, and recommend improvements that strengthen overall security.

---

# Company Overview

**Company:** Botium Toys

**Business:** Toy manufacturer and retailer

**Operations:**

- Corporate office
- Retail storefront
- Warehouse
- E-commerce platform

---

# Audit Scope

The audit covers the entire security program of Botium Toys, including:

- Employee devices
- Internal network
- Internet access
- Servers and databases
- Business systems
- Data storage
- Legacy systems
- Warehouse assets
- Storefront operations
- Physical security controls

---

# Audit Goals

The objectives of the audit are to:

- Review current IT assets.
- Evaluate existing administrative, technical, and physical controls.
- Identify missing security controls.
- Assess compliance with security regulations.
- Recommend improvements to reduce organizational risk.

---

# Current Assets

The IT department manages the following assets:

- Employee desktops and laptops
- Smartphones
- Remote workstations
- Headsets and peripherals
- Surveillance cameras
- Internal network
- Internet services
- Accounting system
- Database system
- Security systems
- E-commerce platform
- Inventory management system
- Data storage
- Legacy systems
- Warehouse inventory

---

# Risk Assessment

## Risk Description

Botium Toys currently has inadequate asset management and several missing security controls. As a result, the organization may not fully comply with U.S. and international security regulations.

## Risk Score

**8 / 10 (High Risk)**

## Major Risks Identified

- Poor asset management
- No least privilege implementation
- No separation of duties
- No encryption for customer payment data
- No Intrusion Detection System (IDS)
- No disaster recovery plan
- No data backups
- Weak password policy
- No centralized password management
- Inconsistent legacy system maintenance

---

# 1. Controls Assessment Checklist

| Control | Implemented? | Notes |
|----------|--------------|-------|
| Least Privilege | ❌ No | Employees have unnecessary access to internal and customer data. |
| Disaster Recovery Plans | ❌ No | No disaster recovery or business continuity plan exists. |
| Password Policies | ❌ No | Password policy exists but does not meet modern security standards. |
| Separation of Duties | ❌ No | Duties and access permissions are not separated. |
| Firewall | ✔️ Yes | Firewall is configured with appropriate security rules. |
| Intrusion Detection System (IDS) | ❌ No | No IDS has been deployed. |
| Backups | ❌ No | Critical business data is not backed up. |
| Antivirus Software | ✔️ Yes | Antivirus software is installed and monitored regularly. |
| Manual Monitoring (Legacy Systems) | ✔️ Yes | Legacy systems are monitored manually, but without a regular schedule. |
| Encryption | ❌ No | Customer payment information is not encrypted. |
| Password Management System | ❌ No | No centralized password management solution exists. |
| Locks (Office, Storefront, Warehouse) | ✔️ Yes | Physical locations are protected with secure locks. |
| CCTV Surveillance | ✔️ Yes | CCTV surveillance is installed throughout the facility. |
| Fire Detection / Prevention | ✔️ Yes | Fire alarms and prevention systems are operational. |

---

# 2. Compliance Assessment Checklist

## PCI DSS

| Best Practice | Implemented? | Notes |
|---------------|--------------|-------|
| Only authorized users access credit card information | ❌ No | All employees currently have access to internal data. |
| Credit card information is stored and processed securely | ❌ No | Payment information is stored internally without sufficient protection. |
| Encryption protects payment data | ❌ No | Encryption has not been implemented. |
| Secure password management policies | ❌ No | Weak password policy and no centralized password management. |

---

## GDPR

| Best Practice | Implemented? | Notes |
|---------------|--------------|-------|
| EU customer data is kept private and secure | ❌ No | Missing access controls and encryption increase privacy risks. |
| Breach notification within 72 hours | ✔️ Yes | A notification plan has been established. |
| Data classification and inventory | ❌ No | Assets and data are not properly classified or inventoried. |
| Privacy policies and procedures | ✔️ Yes | Privacy policies have been documented and enforced. |

---

## SOC 1 / SOC 2

| Best Practice | Implemented? | Notes |
|---------------|--------------|-------|
| User access policies established | ❌ No | Access control policies have not been implemented. |
| Sensitive data (PII/SPII) remains confidential | ❌ No | Missing encryption and unrestricted access expose sensitive information. |
| Data integrity ensured | ✔️ Yes | The IT department has implemented integrity controls. |
| Data available to authorized users | ✔️ Yes | Systems are available and operational for authorized users. |

---

# 3. Summary & Recommendations

The audit shows that Botium Toys has implemented some basic technical and physical controls, including firewalls, antivirus software, CCTV surveillance, and fire prevention systems. However, many important administrative and technical security controls are still missing.

These gaps increase the organization's risk of data breaches, regulatory penalties, and business disruption.

## Administrative Controls

- Implement Least Privilege access.
- Introduce Role-Based Access Control (RBAC).
- Enforce Separation of Duties.
- Create a Disaster Recovery Plan.
- Strengthen password policies.
- Enable Multi-Factor Authentication (MFA).

---

## Technical Controls

- Deploy an Intrusion Detection System (IDS).
- Encrypt sensitive customer and payment data.
- Implement automated backups.
- Use a centralized Password Management System.
- Schedule regular maintenance for legacy systems.

---

## Physical Controls

- Continue maintaining office locks and CCTV surveillance.
- Regularly inspect fire detection and prevention systems.
- Document and test physical security procedures.

---

## Compliance Improvements

- Implement PCI DSS requirements for payment security.
- Improve GDPR compliance through better data classification and access controls.
- Strengthen SOC 1 and SOC 2 controls by implementing user access policies and protecting sensitive information.

---

# Conclusion

The internal security audit identified several high-risk security and compliance gaps within Botium Toys. While the organization has implemented a few essential controls, it must improve access management, encryption, disaster recovery, password security, and monitoring to better protect its systems and customer data.

Implementing these recommendations will significantly strengthen Botium Toys' security posture and support future business growth.