# Flare VM profile
Profile file for [Flare VM](https://github.com/fireeye/flare-vm)
## Requirements
Chocolatey now requires PowerShell v3 (or higher) and .NET 4.0 (or higher) due to recent upgrades to TLS 1.2. Please ensure .NET 4+ and PowerShell v3+ are installed prior to attempting FLARE VM installation. Below are links to download .NET 4.5 and WMF 5.1 (PowerShell 5.1).

* .NET 4.5 [https://www.microsoft.com/en-us/download/details.aspx?id=30653](https://www.microsoft.com/en-us/download/details.aspx?id=30653)
* WMF 5.1 [https://www.microsoft.com/en-us/download/details.aspx?id=54616](https://www.microsoft.com/en-us/download/details.aspx?id=54616)
## Installation
* Create and configure a new Windows Virtual Machine
* Take Snapshot of your machine
* Download and copy [`install.ps1`](https://github.com/fireeye/flare-vm/blob/master/install.ps1) on to your new VM
* Download and copy [`profile.json`](https://raw.githubusercontent.com/av-gantimurov/flarevm-pkg/master/profile.json) on to your new VM
* Download and copy [`flarevm.installer.flare`](https://github.com/fireeye/flare-vm/tree/master/flarevm.installer.flare) directory on to your new VM
* Open Powershell as an Administrator
* Enable script execution by running the following command:
    * `Set-ExecutionPolicy Unrestricted`
* Finally, execute the installer by providing `profile.json` using the `-profile_file` switch, assuming `profile.json`, `install.ps1` and `flarevm.installer.flare` are all in the same directory:
  * `.\install.ps1 -profile_file profile.json`
  * Optionally, you can also pass the following flags:
    * `-password <current_user_password>`: Use the specified password instead of prompting user
