# Harden-Windows-Server
Hardening GPO's Windows Server 2025

There is a new way of Hardening Windows Server 2025. Via OSConfig: [osconfig-how-to-configure-security-baselines](https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure)

Because not everybody is willing to use the new way via OSConfig to configure those settings yet I converted the Security Baseline to GPO's! 

I used the latest OSConfig from Microsoft (november 2024) - [SecurityBaseline_WindowsServer_2025-2411](https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv)

For updated information see topic Work Done (WHATS NEW) in this README.md

## How did I do this?
I used the Microsoft Security Baseline 2022 Member Server from the [Microsoft Security Compliance Toolkit 1.0](https://www.microsoft.com/en-us/download/details.aspx?id=55319) as a starter and changed and added all values from the OSConfig .csv file. I have added an .ADMX and .ADML file for the settings that I could nog find. (zzz.ADMX and zzz.ADML)
If you use the MS Baseline 2022 policies you should also import the templates inside the /zip file! 
- admpwd.admx (and .adml)
- MSS-legacy.admx (and .adml)
- SecGuide.admx (and .adml)

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
- GPO - Create Security Baseline Server 2025 - Domain Controller
- GPO - Create Security Baseline Server 2025 - Standalone
- POWERSHELLSCRIPT - Create powershell script which "backups" tatooing GPO settings before you apply the security baseline
- CHECK - What happens if you enable and disable an tatooing OSConfig setting (and with GPO)
- CHECK - Compare GPO's with [DoD GPO's](https://public.cyber.mil/stigs/gpo/)

## Work Done (WHATS NEW)
- Remove Security Baseline Server 2022 from this GPO (so it only contains the settings Baseline Server 2025 settings) :ok_hand:
- NEW-CHECKSID - In the .Baseline of 2025 there are "strange" sids which still should be solve :

S-1-5-83-0	(NT VIRTUAL MACHINE\Virtual Machines)

S-1-5-82-3006700770-424185619-1745488364-794895919-4004696415  (IIS APPPOOL\DefaultAppPool)

S-1-5-80-3139157870-2983391045-3678747466-658725712-1809340420  (NT SERVICE\WdiServiceHost)

## Files inside this Repository:
FOLDER: **ROOT**
- Windows Server-2022-Member (Exclusive).csv - contains DELTA settings between 2025 and 2022 security baseline. 

FOLDER: **Windows Server-2025-Security-Baseline-v1.0\Templates**
- contains the "old" used Windows Server 2022 Security Baseline templates
- zzz.admx and zzz.adml - Extra policies (which could not be found in the default admx files)

FOLDER: **Windows Server-2025-Security-Baseline-v1.0\GPOs**
- **{C58A0E84-B17B-449B-A327-DF770732F06E}** - Backup of GPO - Microsoft Security Baseline Windows Server 2025 - Member Server
- **{414E1C75-03FD-4367-B1B8-2DC8170AF06D}** - Backup of GPO - Microsoft Security Baseline Windows Server 2025 - Member Server (incl. W2022 Member server settings)
- (NEEDS TO BE DONE) - Backup of GPO - Microsoft Security Baseline Windows Server 2025 - Domain Controller

## Liability

**All GPO's are provided as-is and you use them at your own risk.**

## Contribute

I would be happy to extend the collection of GPO's. Just open an issue or
send me a pull request.

And If you like you can always [buy me a coffee](https://buymeacoffee.com/ronaldnl76) :) 

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
