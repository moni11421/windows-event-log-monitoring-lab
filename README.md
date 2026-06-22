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

## Author

Mohan R
SOC Analyst Home Lab Project
