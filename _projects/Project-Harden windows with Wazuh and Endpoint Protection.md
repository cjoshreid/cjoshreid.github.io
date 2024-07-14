---
layout: page
title: "Project: Hardening Windows 10 with Wazuh and Endpoint Protection"
date: 2023-07-14
---
# Project Portfolio: Strengthening Windows 10 Security with Wazuh and Endpoint Protection

## Project Overview
The goal of this project was to enhance the security of a Windows 10 machine in my home lab by leveraging Wazuh vulnerability detection, listing and patching identified CVEs, and implementing Microsoft's traditional endpoint protection solutions for a layered security approach.

### 1. Wazuh Vulnerability Detection and Patching
- **Objective:** Identify and patch vulnerabilities on the Windows 10 machine using Wazuh's vulnerability detection capabilities.
- **Background:** The Windows 10 machine was a crucial component in my home lab, and maintaining its security was paramount. Wazuh's ability to detect vulnerabilities provided an opportunity to proactively address potential risks.
- **Implementation:**
  - Integrated Wazuh agent on the Windows 10 machine to collect security events.
  - ENABLED THE VULNERABILITY DETECTOR
       ```xml
       <vulnerability-detector>
      <enabled>yes</enabled>
      <interval>5m</interval>
      <min_full_scan_interval>6h</min_full_scan_interval>
      <run_on_start>yes</run_on
  - Leveraged Wazuh's vulnerability detection to identify and list Common Vulnerabilities and Exposures (CVEs) affecting the system.
    - Vulnerability Scan Results of a Fresh Install:
        - Critical: 31
         -  High: 423
         - Medium: 161
         - Low: 4
  - Collaborated with the Windows Update service to apply necessary patches and updates to mitigate identified vulnerabilities.

### 2. Endpoint Protection with Microsoft Defender
- **Objective:** Strengthen the Windows 10 machine's defense mechanisms by configuring and optimizing Microsoft Defender.
- **Background:** In addition to Wazuh's capabilities, integrating Microsoft Defender provided an additional layer of protection against various threats.
- **Implementation:**
  - Configured Microsoft Defender for real-time antivirus and anti-malware protection.
  - Enabled and customized Windows Defender Firewall settings to control incoming and outgoing network traffic.
  - Scheduled regular system scans to identify and mitigate potential threats.

### 3. Key Achievements and Outcomes
- **Effective Vulnerability Management:**
  - Wazuh's vulnerability detection facilitated a systematic approach to identifying and addressing security vulnerabilities on the Windows 10 machine.
  - Patches and updates applied in a timely manner contributed to a more resilient system.

- **Layered Security Approach:**
  - Integration of Wazuh and Microsoft Defender established a comprehensive defense strategy against a wide range of threats, including vulnerabilities and malware.
  - Microsoft Defender's real-time protection complemented Wazuh's capabilities, providing a multi-faceted security framework.

### 4. Lessons Learned
- **Continuous Monitoring is Key:**
  - Regularly monitoring Wazuh alerts and Microsoft Defender reports is essential for maintaining an effective security posture.
  - Continuous vigilance helps in promptly addressing emerging threats and vulnerabilities.

- **Collaboration of Tools:**
  - The synergy between Wazuh and Microsoft Defender showcased the value of combining different security tools to create a more resilient and adaptive security environment.

### 5. Future Enhancements
- **Integrate Threat Intelligence Feeds:**
  - Enhance Wazuh's capabilities by incorporating threat intelligence feeds for more context-aware security alerts.
  
- **Implement Application Whitelisting:**
  - Explore the implementation of application whitelisting on the Windows 10 machine for additional control over executable files.
 
- **Implement Data Backups:**
  - Explore the implementation of data backups of the Windows 10 machine for protection against ransomware encryption attack.

### 6. Conclusion
This project successfully fortified the security posture of the Windows 10 machine through a collaborative approach involving Wazuh vulnerability detection and Microsoft Defender. The combination of proactive vulnerability management and real

### References:
Online tutorials, ChatGPT, Wazuh documentation, Microsoft Defender documentation.

### Screenshots:

Example of Wazuh Vulnerability Detection Alerts
  ![screenshot](screen.png)
  
Details of CVE
  ![screenshot](example.png)
  
Updating and Patching System

   ![screenshot](update.png)

Windows Defender

   ![screenshot](security.png)
  
Results of Patching CVEs using Wazuh and Windows Update
  ![screenshot](results.png)
    ![screenshot](afterlist.png)
