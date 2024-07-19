---
title: "Pyramid of Pain"
layout: post
date: 2024-7-18 03:06
image: 
headerImage: false
tag:
- tryhackme
- SOC 
category: blog
author: Christopher
description: update
---
# Pyramid of Pain

1. **Hash Values**: Digital fingerprints for files. They help spot bad files or malware.
2. **IP Addresses**: Online addresses of where the attackers are coming from.
3. **Domain Names**: Web addresses attackers are using.
4. **Network Artifacts**: Weird or suspicious things happening on the network.
5. **Host Artifacts**: Changes on your computers, like new registry keys or suspicious files.
6. **Tools**: Software and malware, like password crackers or backdoors.
7. **Tactics, Techniques, and Procedures (TTPs)**: The methods and patterns hackers use to break in.

## How the Pyramid of Pain Works

This pyramid helps defenders know which stuff to block first. Threat actors can easily change hash values and IP addresses. Higher-level stuff like network artifacts, host artifacts, and tools becomes more painful for them to recover from. If you can figure out and block their TTPs, you’re really making their life difficult. Go after TTPs using smart intel and frameworks like MITRE ATT&CK.

## Test Each Level of the Pyramid

1. **Hash Values**: Check if your malware detection works.
2. **IP Addresses**: See if your network blocks shady IPs.
3. **Domain Names**: Test connections to dodgy domains.
4. **Network Artifacts**: Look for weird network traffic.
5. **Host Artifacts**: Simulate malware changes on your systems.
6. **Tools**: Try using hacker tools to see if they get blocked.
7. **TTPs**: Run full-on attack simulations to cover all the bases.

