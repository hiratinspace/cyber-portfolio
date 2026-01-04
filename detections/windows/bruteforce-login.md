# Detection: Possible Brute Force Login Attempt

## Description
Detects multiple failed authentication attempts for the same user account within a short time window.

## Data Source
- Windows Security Log
- Event ID: 4625 (Failed Logon)

## Detection Logic
Trigger when:
- Multiple Event ID 4625 entries
- Same username
- Occur within a short time window (e.g., 5 minutes)

## Why This Matters
Repeated failed logins may indicate:
- Password guessing
- Credential stuffing
- Unauthorized access attempts

## False Positives
- Users mistyping passwords
- Automated services with bad credentials

## Severity
Medium

## MITRE ATT&CK Mapping
- T1110 — Brute Force
