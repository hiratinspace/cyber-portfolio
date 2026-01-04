# Detection: LOLBin Execution via rundll32.exe

## Description
Detects execution of rundll32.exe, a legitimate Windows binary commonly abused by attackers to proxy malicious code execution.

## Data Source
- Sysmon
- Event ID: 1 (Process Create)

## Detection Logic
Trigger when:
- Image ends with `rundll32.exe`

## Why This Matters
rundll32.exe is a living-off-the-land binary (LOLBin) often used to:
- Execute malicious DLLs
- Bypass application allowlists
- Blend in with normal system activity

## False Positives
- Legitimate system processes
- Application installers

## Severity
Medium

## MITRE ATT&CK Mapping
- T1218 — Signed Binary Proxy Execution
