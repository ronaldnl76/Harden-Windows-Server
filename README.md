# Harden-Windows-Server
Hardening GPO's Windows Server 2025

There is a new way of Hardening Windows Server 2025. Via OSConfig: [osconfig-how-to-configure-security-baselines]https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure

Because we don't want to use OSConfig yet I converted the Security Baseline to GPO's.

I used the latest OSConfig from Microsoft (november 2024) - [SecurityBaseline_WindowsServer_2025 24-11]https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv

## GPO's inside this Repository:
- **MSFT Windows Server 2025 - Member Server** - Microsoft Security Baseline Windows Server 2025 - Member Server

- **MSFT Windows Server 2025 - Domain Controller** - Microsoft Security Baseline Windows Server 2025 - Domain Controller (NEEDS TO BE BUILT)


## Liability

**All GPO's are provided as-is and you use them at your own risk.**

## Contribute

I would be happy to extend the collection of GPO's. Just open an issue or
send me a pull request.

### Important Websites:
- [osconfig-how-to-configure-security-baselines]https://learn.microsoft.com/en-us/windows-server/security/osconfig/osconfig-how-to-configure-security-baselines?tabs=configure
- [SecurityBaseline_WindowsServer_2025 24-11]https://github.com/microsoft/osconfig/blob/main/security/SecurityBaseline_WindowsServer_2025-2411.csv

## License

MIT License
Copyright (c) 2023-Present - Ronald Rijerkerk- (ronaldnl76)

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
