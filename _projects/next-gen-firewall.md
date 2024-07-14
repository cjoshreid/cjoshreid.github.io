---
layout: page
title: "Project: Exploring a Next-Generation Firewall with ZenArmor"
date: 2023-07-14
---

Exploring a Next-Generation Firewall with OPNsense and ZenArmor.

# Project: Exploring a Next-Generation Firewall with OPNsense and ZenArmor

## Project Overview

The objective of this project was to explore the capabilities of a next-generation firewall by integrating ZenArmor with OPNsense within my home lab. The project involved reloading a fresh install of OPNsense within VirtualBox and excluding all the previously configured policies and custom rules. Unfortantly you are unable to have suricata and zenarmor run simultaneously but I wanted to install ZenArmor to evaluate its features.

### Evaluation Notes

- **Fresh Installation:**
  - Reloaded a fresh install of OPNsense to ensure compatibility with ZenArmor.
  - Excluded previously configured policies and custom rules due to incompatibility with Suricata and ZenArmor.

- **ZenArmor Interface:**
  - ZenArmor's user interface was incredibly easy to use, clean UI even for non-technical people.

- **Traffic Logging:**
  - The logs resemble a Intrusion Detection System (IDS) with a real-time view of live traffic. Again, a very nice interface.
  - The level of detail; country of origin, destination, applications, etc makes the identification of odd or unusual connections easy and a place to begin investigation. Although I wish it had the ability to automaticly flag such connections. Maybe a AI feature that could be added later?

- **Application and Web Control:**
  - A next generation firewall really gives you the power of honing in with application control and web control instead of solely relying on rule-based firewall rules.
  - Enables you to protect the network, not just with general rule sets, but by preventing users from unathorized site or application access that could introduce threats such as malware.
  - These would be extremely useful features in a office or business network.

- **Limitations:**
  - Sadly I could not fully test zenarmor due to the use of a free account. I was prevented from integrating it with Wazuh and did not have access to some of the security policy options.

## Key Achievements and Outcomes

**Evaluation of ZenArmor:**
- Explored the capabilities of ZenArmor in enhancing the OPNsense firewall.
- Recognized the significance of application and web control features for network security.

**User Interface and Traffic Monitoring:**
- Appreciated the user-friendly interface and real-time traffic monitoring capabilities of ZenArmor.

**Insights for Business Networks:**
- Identified the potential benefits of ZenArmor features for enhancing security in office or business network environments.

## Lessons Learned

**Compatibility and Limitations:**
- Understood the challenges of compatibility between different security tools and the constraints of free account limitations.

**Automated Flagging:**
- Identified the need for automated flagging of suspicious connections for more efficient threat response.

## Future Enhancements

- **Advanced Account Access:**
  - Explore advanced features and security policy options with a premium ZenArmor account.

- **Integration with Wazuh:**
  - Investigate possibilities for integrating ZenArmor with Wazuh for enhanced threat detection and response.

 - **Integration with Automation:**
  - Investigate possibilities of automating alerts for unusual connections with scripting or AI.

## Conclusion

This project successfully tested the integration of ZenArmor with OPNsense, providing insights into its user interface, traffic monitoring capabilities, and potential benefits for business networks. The identified limitations and lessons learned will guide future enhancements to further optimize network security.

## References:

[OPNsense documentation](https://docs.opnsense.org), [ZenArmor Official Website](https://www.zenarmor.com), online tutorials, ChatGPT.

### Screenshot:

Installing the Plugins
  ![screenshot](sensei.png)
  


  
