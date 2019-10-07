# Introduction to Windows Subsystem for Linux

---

## Links & Resources

- [install-win10](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- [install-manual](https://docs.microsoft.com/en-us/windows/wsl/install-manual)
- [init-distro](https://docs.microsoft.com/en-us/windows/wsl/initialize-distro)

---
Install the Windows Subsystem for Linux

Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:

    Open PowerShell as Administrator and run:
    PowerShell

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Restart your computer when prompted.
