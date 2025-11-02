Summary:
The group performs system and network discovery using built-in Windows commands to gather environment info.

Related Sigma Rules:

T1082_System_Information_Discovery.yml

T1018_Remote_System_Discovery.yml

T1083_File_and_Directory_Discovery.yml

Detection Notes:

Detect execution of:

systeminfo
nltest /dclist
net group "Domain Admins" /domain
dir /s


Correlate enumeration activity followed by lateral movement or credential access.
