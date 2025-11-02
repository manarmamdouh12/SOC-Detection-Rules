🛡️ SOC Detection Rules

This repository contains a growing collection of detection rules and use cases developed to identify malicious behaviors, tools, and techniques observed in real-world cyberattacks.
Each folder is based on a specific Threat Intelligence Report or APT campaign, with mapped MITRE ATT&CK techniques, corresponding Sigma rules, and detection notes for SOC Analysts.

The goal is to help security teams detect, investigate, and respond to evolving threats by translating threat intelligence into actionable detection logic for SIEM and EDR platforms.

SOC-Detection-Rules/
├── Cavalry_Werewolf_APT/                 → Detection package for Picus APT report
│   ├── README.md                         → Summary of the campaign and key techniques
│   ├── Detection_UseCases/               → Markdown files explaining each ATT&CK stage
│   └── Techniques/                       → Sigma rules per MITRE ATT&CK ID
│
├── Other_APT_Campaigns/                  → Future additions (e.g., FIN7, APT29, etc.)

🚀 Objective

To build an open-source detection knowledge base that bridges Threat Intelligence → Detection Engineering, providing SOC analysts with ready-to-deploy Sigma rules and investigation insights derived from real adversary behavior.

🧠 Key Highlights

Mapped to MITRE ATT&CK framework.

Designed for SIEM platforms (e.g., Microsoft Sentinel, ELK, Splunk).

Continuously updated with new campaigns and techniques.

Includes investigation guidance and response context.

👩‍💻 Author

Manar Mamdouh – SOC Analyst | SOC Analyst Engineer
Focused on transforming threat intelligence into effective, real-world detections.
