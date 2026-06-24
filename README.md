# windows-event-log-monitoring-lab
Windows Event Log Monitoring and Threat Hunting Lab using Sysmon and Event Viewer

# Windows Event Log Monitoring Lab using Sysmon

## Project Overview

This project demonstrates Windows endpoint monitoring using Sysmon and Event Viewer.

The objective was to generate and investigate Windows security events commonly analyzed by SOC Analysts.

## Tools Used

* Windows 11 Virtual Machine
* VMware Workstation
* Sysmon
* Event Viewer
* PowerShell

## Event IDs Investigated

### Event ID 1 - Process Creation

Investigated:

* Notepad.exe
* PowerShell.exe
* Whoami.exe
* Hostname.exe
* Ipconfig.exe
* Chrome.exe

### Event ID 11 - File Creation

Investigated file creation activity and tracked process execution responsible for creating files.

### Event ID 22 - DNS Query

Investigated DNS lookups and domain resolution activity.

## Key Findings

* Process creation events reveal user and process activity.
* DNS query events help identify external communications.
* File creation events help track malware and suspicious files.
* Parent-child process relationships are useful for threat hunting.

## Skills Demonstrated

* Windows Log Analysis
* Sysmon Monitoring
* Event Viewer Investigation
* Threat Hunting
* Process Analysis
* Incident Investigation

## Threat Hunting Findings

### Finding 1 - PowerShell Reconnaissance

Observed PowerShell spawning:

* whoami.exe
* hostname.exe
* ipconfig.exe

This activity is commonly seen during attacker reconnaissance after initial access.

### Finding 2 - DNS Resolution

Observed ping.exe generating DNS queries for google.com.

Sysmon Event ID 22 successfully captured the DNS resolution activity.

### Finding 3 - File Creation Monitoring

Observed file creation events through Sysmon Event ID 11.

The process responsible for file creation was successfully identified using Event Viewer.

### Finding 4 - Browser Activity

Observed chrome.exe process creation and related network activity.

Process execution was tracked using Sysmon Event ID 1.


## Author

Mohan R
SOC Analyst Home Lab Project
