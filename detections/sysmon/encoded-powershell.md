# Detection: Encoded PowerShell Execution

## Description
Detects PowerShell processes launched with encoded command arguments, which are commonly used to obscure malicious activity.

## Data Source
- Sysmon
- Event ID: 1 (Process Create)

## Detection Logic
Trigger when:
- Image ends with `powershell.exe`
- AND CommandLine contains `-EncodedCommand`

## Example Indicators
- `powershell.exe -EncodedCommand <Base64 string>`

## Why This Matters
Encoded PowerShell is frequently used to:
- Evade basic logging
- Obfuscate malicious payloads
- Bypass simple command-line inspection

While it can be legitimate, it is a high-signal behavior that warrants investigation.

## False Positives
- Administrative scripts
- Automation tools

## Severity
Medium–High

## MITRE ATT&CK Mapping
- T1059.001 — Command and Scripting Interpreter: PowerShell
