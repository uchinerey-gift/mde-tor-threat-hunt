# 🕵🏾‍♀️ Microsoft Defender Advanced Hunting — Unauthorized TOR Usage Lab

![Status](https://img.shields.io/badge/Lab-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Microsoft%20Defender-blue)
![Tools](https://img.shields.io/badge/Tools-KQL%20%7C%20PowerShell-orange)
![Focus](https://img.shields.io/badge/Focus-Threat%20Hunting%20%7C%20EDR-lightgrey)

A step-by-step Microsoft Defender for Endpoint threat-hunting lab demonstrating detection of unauthorized TOR browser usage across file, process, and network telemetry.

---

## Step 1 — Device Visibility Validation

Confirmed the Windows endpoint was visible and actively reporting in Microsoft Defender to ensure telemetry would be captured for the investigation.

Evidence file: `01_MDE_Device_Visible_In_Defender_Portal.png`  
![01_MDE_Device_Visible_In_Defender_Portal](evidence/screenshots/01_MDE_Device_Visible_In_Defender_Portal.png)

---

## Step 2 — Defender Sensor Validation

Verified the Microsoft Defender for Endpoint sensor (Sense service) was running to confirm endpoint telemetry ingestion.

```powershell
Get-Service -Name Sense
Evidence file: 02_Windows_Sense_Service_Running.png

Step 3 — TOR Installer Download
Downloaded the TOR Browser installer to the endpoint to generate file creation and download telemetry.

powershell
Copy code
# TOR installer downloaded via browser to the Downloads directory
Evidence file: 03_TOR_Installer_Downloaded_In_Downloads.png

Step 4 — TOR Installer Filename Confirmation
Identified and documented the exact TOR installer filename and version to ensure accurate KQL hunting.

powershell
Copy code
# Verified exact installer filename in the Downloads folder
Evidence file: 04_TOR_Installer_Filename_Confirmed.png

Step 5 — Silent TOR Installation Execution
Executed the TOR installer using silent installation flags to simulate unauthorized background software installation.

powershell
Copy code
tor-browser-windows-x86_64-portable-15.0.3.exe  /S
Evidence file: 05_TOR_Silent_Install_Command_Executed.png

Step 6 — TOR Browser Execution
Launched TOR Browser to generate process execution telemetry associated with anonymization tooling.

powershell
Copy code
# TOR Browser launched from extracted directory
Evidence file: 06_TOR_Browser_Launched.png

Step 7 — TOR Network Activity Generation
Generated anonymized outbound network activity by browsing through TOR to produce network telemetry.

powershell
Copy code
# Active browsing session through TOR network
Evidence file: 07_TOR_Network_Activity_Generated.png

Step 8 — Suspicious File Creation and Deletion
Created and deleted a suspicious file using PowerShell to simulate artifact staging and anti-forensics behavior.

powershell
Copy code
cd $env:USERPROFILE\Desktop
New-Item -Name "tor-shopping-list.txt" -ItemType File
Add-Content -Path "tor-shopping-list.txt" -Value "fake item 1"
Add-Content -Path "tor-shopping-list.txt" -Value "fake item 2"
Remove-Item -Path "tor-shopping-list.txt"
Evidence file: 08-09_TOR_Shopping_List_File_Create_Modify_Delete_PowerShell.png

