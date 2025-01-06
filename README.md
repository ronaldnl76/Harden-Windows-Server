# Harden-Windows-Server
Hardening GPO's Windows Server 2025

There is a new way of Hardening Windows Server 2025. Via OSConfig: [osconfig-how-to-configure-security-baselines](https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure)

Because we don't want to use OSConfig yet I converted the Security Baseline to GPO's!

I used the latest OSConfig from Microsoft (november 2024) - [SecurityBaseline_WindowsServer_2025-2411](https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv)

## How did I do this?
I used the Microsoft Security Baseline 2022 Member Server from the [Microsoft Security Compliance Toolkit 1.0](https://www.microsoft.com/en-us/download/details.aspx?id=55319) as a starter and changed and added all values from the OSConfig .csv file. I have added an .ADMX and .ADML file for the settings that I could nog find. (zzz.ADMX and zzz.ADML)

There is an new .csv file added with all settings from the CSV file categorized into:
- NEW - these are new settings compared to those of the Security Baseline of Windows Server 2022
- NEW-CHECKSID - In the .Baseline of 2025 there are "strange" sids which still should be solved
- CHANGED - these settings differ to those of the Security Baseline of Windows Server 2022
- Custom ADMX - Use Custom ADMX file
- TODO - AuditBackupAndRestorePrivilege registry key differs from .csv file.
- Used settings from 2022 - Used the settings from the Security Baseline of Windows Server 2022
- DOMAIN CONTROLLER ONLY - Settings that needs to be configured on Domain Controllers (Still need to be done)
- CHANGE to your OWN! - These settings needs to be edited to your own needs.

## Still some work to do:
- There are 2 items that still needs some attention
AuditBackupAndRestorePrivilege registry key differs from .csv file.
RestrictClientsAllowedToMakeRemoteCallsToSAM - used the settings from 2022 MSFT
- Remove Security Baseline Server 2022 from this GPO (so it only contains the settings Baseline Server 2025 settings)
- Create Security Baseline Server 2025 - Domain Controller GPO 
- NEW-CHECKSID - In the .Baseline of 2025 there are "strange" sids which still should be solved


## Files inside this Repository:
- **MSFT Windows Server 2025 - Member Server** - Backup of GPO - Microsoft Security Baseline Windows Server 2025 - Member Server

- **MSFT Windows Server 2025 - Domain Controller** - Backup of GPO - Microsoft Security Baseline Windows Server 2025 - Domain Controller
(NEEDS TO BE DONE)


## Liability

**All GPO's are provided as-is and you use them at your own risk.**

## Contribute

I would be happy to extend the collection of GPO's. Just open an issue or
send me a pull request.

### Important Websites:
- [osconfig-how-to-configure-security-baselines](https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure)
- [SecurityBaseline_WindowsServer_2025-2411](https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv)
- [Microsoft Security Compliance Toolkit 1.0](https://www.microsoft.com/en-us/download/details.aspx?id=55319)

## License
  
    MIT License:

    Copyright (c) 2025-Present - Ronald Rijerkerk - (ronaldnl76)

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
  
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
