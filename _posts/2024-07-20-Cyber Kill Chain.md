---
title: "Cyber Kill Chain"
layout: post
date: 2024-7-20 02:16
image: 
headerImage: false
tag:
- tryhackme
- SOC 
- framework
category: blog
author: Christopher
description: update
---
# Cyber Kill Chain

Identify and stop enemy activity.

## Phase 1: Reconnaissance
A threat actor scopes out their target, looking for any weaknesses to exploit. Using OSINT, they gather email addresses, user IDs, physical locations, and software info. The more data they collect, the better they can tailor their attack, making it harder to spot and more likely to succeed.

## Phase 2: Weaponization
Using the information from reconnaissance, the attacker gathers and/or builds malware, ransomware, viruses, or worms. They might also set up back doors to maintain access, even if their initial entry point gets discovered and shut down by the network admins.

## Phase 3: Delivery
Launching the attack. This could involve sending malicious email attachments or links designed to trick users into opening them. Social engineering tactics often come into play here to boost the chances of success.

## Phase 4: Exploitation
This is when the malicious code actually runs on the victim’s system.

## Phase 5: Installation
The malware gets installed on the victim’s system, marking a critical point in the attack. The attacker now has a foothold and can start taking control.

## Phase 6: Command and Control
The attacker uses the malware to remotely control the infected device or identity within the network. They might also move laterally, spreading their reach and setting up additional entry points.

## Phase 7: Actions on Objective
This could be stealing data, destroying information, encrypting files, or exfiltrating sensitive content.

