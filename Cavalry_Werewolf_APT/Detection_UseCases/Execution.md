Summary:
The attackers execute encoded PowerShell commands and scripts to download and run the next-stage payloads. They may use CMD or PowerShell with -ExecutionPolicy Bypass, -EncodedCommand, or hidden window parameters.

Related Sigma Rules:

T1059.001_PowerShell_Execution.yml

T1059.003_Windows_Command_Shell_Execution.yml

Detection Notes:

Hunt for PowerShell or cmd instances launched with:

-ep bypass, -EncodedCommand, -WindowStyle Hidden


Detect child processes spawned from Office applications.

Correlate process lineage with network activity (possible downloader).
