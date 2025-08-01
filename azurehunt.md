---
title: Advanced Threat Hunting Cheat Sheet
layout: home
parent: <b>Security Tools</b>
---

# Advanced Threat Hunting Cheat Sheet

#### Disclaimer

The sample scripts are not supported under any Microsoft standard support program or service.  
These scripts are provided AS IS without warranty of any kind.

---

| Query Purpose | Query Content | Notes |
|---------------|--------------|-------|
| Find endpoints communicating to a specific domain. | `let Domain = "http://domainxxx.com"; DeviceNetworkEvents | where Timestamp > ago(7d) and RemoteUrl contains Domain | project Timestamp, Device[...]` |  |
| Finds PowerShell execution events that could involve a download. | `union DeviceProcessEvents, DeviceNetworkEvents | where Timestamp > ago(7d) | where FileName in~ ("powershell.exe", "powershell_is[...]` |  |
| Find scheduled tasks created by a non-system account | - | - |
| Find possible clear text passwords in Windows registry | - | - |
| Lookup process executed from binary hidden in Base64 encoded file | - | - |
| Search for applications who create or update an 7Zip or WinRAR archive when a password is specified. | - | - |
| Search Device Events by IP address | - | - |
| SList Devices with Schedule Task created by Virus | - | - |
| List Device contained Virus File Name | - | - |
| List Devices with Phishing File extension (double extension) as .pdf.exe, .docx.exe, .doc.exe, .mp3.exe | - | - |
| List Device blocked by Windows Defender ExploitGuard | - | - |
| List All Files Create during the last hour | - | - |
| List Device who has a specific File Hash | - | - |
| List IP address blocked by FW rule | - | - |
| Look for public the IP addresses of devices that failed to logon multiple times, using multiple accounts, and eventually succeeded. | - | - |
| Look for machines failing to log-on to multiple machines or using multiple accounts | - | - |
| List all devices named start with prefix FC- | - | - |
| List Windows Defender Scan Actions completed or Cancelled | - | - |
| List Devices access to bad URL | - | - |
| List All URL access by a Device named contained the word FC-DC | - | - |
