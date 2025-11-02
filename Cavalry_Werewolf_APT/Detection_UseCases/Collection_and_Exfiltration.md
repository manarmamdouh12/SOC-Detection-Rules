Summary:
Data collected from target systems is compressed using tools like WinRAR and exfiltrated via HTTP or cloud services.

Related Sigma Rules:

T1560_Data_Compression_Utility_Usage.yml

T1041_Exfiltration_Over_HTTPS.yml

Detection Notes:

Monitor command-line executions of WinRAR creating archives in sensitive folders.

Detect uploads or outbound connections to file-sharing or cloud services (e.g., bublup.com, Amazon S3).

Correlate large outbound data transfer volume with previous discovery or collection phases.
