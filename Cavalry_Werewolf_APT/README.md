Cavalry Werewolf APT – Detection Use Cases Repository

Source: https://www.picussecurity.com/resource/blog/cavalry-werewolf-apt

Author: Manar Mamdouh

Date: November 2025

🧠 Threat Overview

The Cavalry Werewolf APT campaign leverages phishing-based initial access and multi-stage malware delivery to compromise victims within governmental and strategic sectors. Attackers rely heavily on social engineering, PowerShell-based payload execution, and Telegram-based command-and-control (C2) channels to maintain persistence and exfiltrate sensitive data.

🕵️‍♀️ Detection Coverage Summary

This repository contains Sigma rules that detect key behaviors and techniques observed in the Cavalry Werewolf campaign.
The detections are mapped to MITRE ATT&CK techniques across multiple attack stages:

1. Initial Access

Detects phishing emails using fake or urgent document names intended to deceive users.

2. Execution

Identifies PowerShell commands using ExecutionPolicy Bypass or EncodedCommand for defense evasion.

Detects PowerShell download cradles used to fetch and execute payloads remotely.

Flags Base64-encoded PowerShell invoke executions used for obfuscation.

Detects cmd.exe executions from temporary or public directories often abused for staging payloads.

Identifies cmd.exe processes spawned from non-interactive parent processes, indicating potential automated or scripted attacks.

3. Persistence

Detects registry persistence mechanisms using Run keys in non-standard directories, a common stealth technique.

4. Discovery and Reconnaissance

Flags anomalous reconnaissance commands executed from temporary or user directories, often used by downloaded malware.

5. Command and Control (C2)

Detects Telegram Bot API requests and other suspicious Telegram network communications used as C2 channels.

Identifies non-browser Telegram traffic communicating with Telegram servers over HTTPS.

Detects file downloads from Telegram infrastructure, used to deliver payloads or tools.

Flags the execution of SOCKS5 proxy tools, commonly used to tunnel or relay malicious traffic.

6. Collection and Exfiltration

Detects the creation of archive files within Outlook cache directories, a sign of data collection prior to exfiltration.
