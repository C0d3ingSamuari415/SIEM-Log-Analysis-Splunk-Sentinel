# Investigation Report: Failed Login Analysis

## Summary
Analyzed authentication logs to identify repeated failed login attempts from a single IP address, indicating a potential brute-force attack.

## Indicators
- Multiple failed logins for root/admin
- Source IP: 192.168.1.45
- Repeated attempts within seconds

## Tools Used
- Splunk (query in /splunk_queries)
- Azure Sentinel (query in /sentinel_kql)
- Linux log parsing

## Findings
- 4 failed attempts in under 10 seconds
- Targeted accounts: admin, root
- Attack pattern consistent with brute-force behavior

## MITRE ATT&CK Mapping
- **T1110 – Brute Force**

## Recommended Actions
- Block offending IP
- Enforce MFA
- Review authentication logs for additional anomalies
