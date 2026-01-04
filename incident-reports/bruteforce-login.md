# Incident Report: Brute Force Login Attempt

## Summary
Multiple failed authentication attempts were observed for a local user account, followed by a successful login.

## Timeline
- 7:01:12 PM – Failed logon (Event ID 4625)
- 7:01:05 PM – Failed logon (Event ID 4625)
- 7:01:16 PM – Successful logon (Event ID 4624)

## Analysis
Repeated authentication failures followed by success may indicate password guessing activity.

## Evidence
- Windows Security Event IDs 4625 and 4624

## Severity
Medium

## Recommendations
- Monitor repeated failed logins
- Apply account lockout thresholds
- Correlate with endpoint telemetry
