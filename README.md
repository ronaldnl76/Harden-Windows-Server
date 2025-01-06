# Harden-Windows-Server
Hardening GPO's Windows Server 2025

There is a new way of Hardening Windows Server 2025. Via OSConfig: [osconfig-how-to-configure-security-baselines]https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure

Because we don't want to use OSConfig yet I converted the Security Baseline to GPO's.

I used the latest OSConfig from Microsoft (november 2024) - [SecurityBaseline_WindowsServer_2025 24-11]https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv

## GPO's inside this Repository:
- **MSFT Windows Server 2025 - Member Server** - This script will generate random password(s) of an given length 
and uses a Dutch open Wordlist to generate those passwords so that they are Safe and human readable.
The wordlist is from OpenTaal. For English you could add your own wordlist E.g. [dwyl](https://github.com/dwyl/english-words)

- **MSFT Windows Server 2025 - Domain Controller** - Microsoft Security Baseline Windows Server 2025 - Domain Controller


## Execution

Enable execution of PowerShell scripts:

    PS> Set-ExecutionPolicy Unrestricted -Scope CurrentUser

Unblock PowerShell scripts and modules within this directory:

    PS> ls -Recurse *.ps*1 | Unblock-File

## Liability

**All GPO's are provided as-is and you use them at your own risk.**

## Contribute

I would be happy to extend the collection of scripts. Just open an issue or
send me a pull request.

### Important Websites:
- [osconfig-how-to-configure-security-baselines]https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure
- [SecurityBaseline_WindowsServer_2025 24-11]https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv

## License

    "THE BEER-WARE LICENSE" (Revision 42):

    As long as you retain this notice you can do whatever you want with this
    stuff. If we meet someday, and you think this stuff is worth it, you can
    buy us a beer in return.

    This project is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
    FITNESS FOR A PARTICULAR PURPOSE.
