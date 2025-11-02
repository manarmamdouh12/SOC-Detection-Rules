Summary:
Cavalry Werewolf uses spear-phishing emails with malicious attachments (macro-enabled Office files or weaponized archives). When opened, the document triggers malicious PowerShell or script execution.

Related Sigma Rules:

T1566.001_Phishing_Attachment.yml

T1204.002_User_Execution_Malicious_File.yml

Detection Notes:

Detect suspicious email attachments with document-like names (.doc, .xls, .zip) followed by PowerShell or cmd execution.

Use mail gateway or EDR telemetry to detect auto-start of macros.
