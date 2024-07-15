---
layout: page
title: "Project Portfolio: Enhancing Network Security with Suricata, OPNsense, and Wazuh"
date: 2023-07-14
---

# Project Portfolio: Enhancing Network Security with Suricata, OPNsense, and Wazuh

## Project Overview
In this project, the goal was to strengthen the network security of the simulated enterprise in my homelab by implementing a comprehensive solution involving Suricata for custom rule creation in OPNsense and integrating Wazuh for advanced threat detection and active response.

### 1. Suricata Custom Rules in OPNsense
- **Objective:** Strengthen network visibility and threat detection by customizing Suricata rules on the OPNsense firewall.
- **Background:** Even with Nmap scans I wasn't always able to detect every interaction on the internal network. I wanted everything to be logged even if it was to be a nuisance alarm I could later adjust.
- **Implementation:**
  - Configured Suricata, an open-source intrusion detection and prevention system, on the OPNsense firewall.
  - Developed and deployed custom rules in Suricata to generate alerts for every interaction with IP addresses within the network.
  - EXAMPLE: *each tested and confirmed with a simple Nmap scan*
    - ALERT - FIREWALL TOUCHED	
	- ALERT - WINDOWS MACHINE TOUCHED	
	- ALERT - LINUX SERVER TOUCHED	
	- ALERT - UBUNTU SERVER TOUCHED

## 2. Wazuh Active Response for Brute Force Protection and Credential Access

- **Objective:** Enhance security measures by implementing active response mechanisms using Wazuh.
- **Background:** I set up an SSH connection between the Windows machine and the Ubuntu server, logging various interactions. Multiple failed login attempts, even as root, were only being logged without a response. Additionally, Wazuh logged several brute force attack attempts from outside the network onto the OPNsense firewall. Active response to these threats was deemed necessary.
- **Implementation:**
  - Integrated Wazuh, an open-source security information and event management (SIEM) tool, into the network infrastructure.
  - Utilized custom active responses in Wazuh to implement dynamic firewall blocking in response to brute force attacks.
  - Configured Wazuh to initiate firewall blocks for IP addresses involved in multiple failed login attempts within a specified time frame.
  
  **EXAMPLE:**
  
  ```xml
  <!-- Firewall Block brute force attempt rule - 87702-->
  <active-response>
    <command>firewall-drop</command>
    <location>local</location>
    <rules_id>87702</rules_id>
    <timeout>no</timeout>
  </active-response>
  
  <!-- Firewall Block incorrect login for 180s - rule 5503-->
  <active-response>
    <command>firewall-drop</command>
    <location>local</location>
    <rules_id>5503</rules_id>
    <timeout>180</timeout>
  </active-response>
  
  <!-- 3 Incorrect Logins within 60 min - Repeat Offenses: rule 5503 -->
  <active-response>
    <command>firewall-drop</command>
    <location>local</location>
    <rules_id>5503</rules_id>
    <timeout>no</timeout>
    <repeated_offenders>
      <minutes>60</minutes>
      <threshold>3</threshold>
    </repeated_offenders>
  </active-response>

- **With this configuration:**
   - When a brute force attack is detected the response is set to firewall-drop.
   - When a user enters an incorrect password their IP address will be blocked from the system for 180s. 
   - When a user enters an incorrect password 3 times within a 60-minute period, their IP address will be blocked from the system permanently.


### 3. Key Achievements and Outcomes
- **Improved Threat Detection:**
  - Suricata's custom rules provided granular visibility into network interactions, enabling swift detection of potential threats.
  - OPNsense, empowered by Suricata, became a robust first line of defense against various network-based attacks.

- **Proactive Brute Force Protection:**
  - Wazuh's active response mechanisms, combined with custom rules, allowed for the immediate identification and mitigation of brute force attacks.
  - Automatic firewall blocking for repeat offenders added an additional layer of security against persistent threats.

- **Efficient Incident Response:**
  - By integrating Suricata and Wazuh, the project facilitated a streamlined incident response process, minimizing the time between threat detection and mitigation.

### 4. Lessons Learned
- **Configuration Accuracy:**
  - Precision in creating custom rules is crucial for effective threat detection. Ensuring accurate configurations in Suricata is essential for minimizing false positives and negatives.

- **Active Response Fine-Tuning:**
  - Continuous refinement of active response mechanisms in Wazuh is necessary to strike a balance between security and user convenience.

### 5. Future Enhancements
- **Incident Investigation Capabilities:**
  - Consider expanding Wazuh's integration with additional security tools to enhance incident investigation capabilities.

- **User Awareness Training:**
  - Implement user awareness programs to educate users about the importance of strong passwords and cybersecurity best practices.

### 6. Conclusion
This project successfully leveraged Suricata, OPNsense, and Wazuh to create a robust network security infrastructure. The combination of custom rules for threat detection and active response mechanisms for immediate mitigation ensures a proactive and efficient defense against various cyber threats. Continuous monitoring, periodic rule adjustments, and user education will contribute to the project's long-term success in maintaining a secure network environment.

## References: 
Online tutorials, ChatGPT, and official documentation of tools used. 

## Screenshots:
Example Log of Suricata Custom Rules during testing
  ![screenshot](https://github.com/cjoshreid/cjoshreid.github.io/blob/1750d6ee04a19c9c7a30d4cc77a2f850bbbf6c86/_projects/images/alerts2.png)
Log of Brute Force Attack  
  ![screenshot](https://github.com/cjoshreid/cjoshreid.github.io/blob/1750d6ee04a19c9c7a30d4cc77a2f850bbbf6c86/_projects/images/bruteforce.png)
Example Log of Login Failures during testing
   ![screenshot](https://github.com/cjoshreid/cjoshreid.github.io/blob/1750d6ee04a19c9c7a30d4cc77a2f850bbbf6c86/_projects/images/loginfail.png)
Log of Login Failures and Active Response  
   ![screenshot](https://github.com/cjoshreid/cjoshreid.github.io/blob/1750d6ee04a19c9c7a30d4cc77a2f850bbbf6c86/_projects/images/loginfailresponse.png)
