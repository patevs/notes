# Introduction to Windows Subsystem for Linux

---

## Links & Resources

- [install-win10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- [install-manual](https://docs.microsoft.com/en-us/windows/wsl/install-manual)
- [init-distro](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro)

https://docs.microsoft.com/en-us/windows/wsl/about?redirectedfrom=MSDN

---

## Install the Windows Subsystem for Linux

Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:

    Open PowerShell as Administrator and run:
    PowerShell

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Restart your computer when prompted.

## Downloading distros via the command line

If you prefer, you can also download your preferred distro(s) via the command line:
Download using PowerShell

To download distros using PowerShell, use the Invoke-WebRequest cmdlet. Here's a sample instruction to download Ubuntu 16.04.
PowerShell

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

Tip

If the download is taking a long time, turn off the progress bar by setting $ProgressPreference = 'SilentlyContinue'

## Installing your distro

If you're using Windows 10 you can install your distro with PowerShell. Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where app_name is the name of your distro .appx file.
Powershell

`Add-AppxPackage .\app_name.appx`

[](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro)

https://conemu.github.io/en/BashOnWindows.html#TLDR
