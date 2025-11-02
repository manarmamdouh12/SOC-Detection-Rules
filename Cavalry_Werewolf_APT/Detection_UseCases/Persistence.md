Summary:
Cavalry Werewolf establishes persistence using registry keys (HKCU\Software\Microsoft\Windows\CurrentVersion\Run) or scheduled tasks that execute their RAT on boot.

Related Sigma Rules:

T1547.001_Registry_RunKey_Autostart.yml

T1053.005_Scheduled_Task_Creation.yml

Detection Notes:

Monitor for new autorun entries referencing suspicious binaries in public directories (e.g., C:\Users\Public\Libraries\).

Detect schtasks.exe or powershell.exe creating new tasks that launch unknown executables.
