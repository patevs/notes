
# PowerShell Customization

> PowerShell is a task automation and configuration management framework from Microsoft, consisting of a command-line shell and associated scripting language.

---

## Links & Resources

- [`awesome-powershell`](https://github.com/janikvonrotz/awesome-powershell)
- [PowerShell Customization](https://hodgkins.io/ultimate-powershell-prompt-and-git-setup)
- [`posh-git`](https://github.com/dahlbyk/posh-git)

[]()

- [Enable Additional Fonts](https://www.howtogeek.com/howto/windows-vista/stupid-geek-tricks-enable-more-fonts-for-the-windows-command-prompt/)
- [Emojis in PowerShell](https://artofshell.com/2016/04/emojis-in-powershell-yes/)
- [Emojis Module](https://www.powershellgallery.com/packages/Emojis/0.1)

---

## Create the PowerShell Profile

To create your `$PROFILE` do the following:

```powershell
# Creates profile if doesn't exist
if (!(Test-Path -Path $PROFILE)){ New-Item -Path $PROFILE -ItemType File }
```

## Install Required Components

In an Administrative PowerShell prompt enter the following:

```powershell
# Set your PowerShell execution policy
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Force
# Install PowerShell Modules
Install-PackageProvider NuGet -MinimumVersion '2.8.5.201' -Force
Set-PSRepository -Name PSGallery -InstallationPolicy Trusted
Install-Module -Name 'posh-git'
# Fix issue with ssh-agent unable to start
Set-Service ssh-agent -StartupType Manual
```

## Generate an SSH Key

```powershell
# Generate the key and put into the your user profile .ssh directory
ssh-keygen -t rsa -b 4096 -C "your@email.com" -f $env:USERPROFILE\.ssh\id_rsa
# Copy the public key. Be sure to copy the .pub for the public key
Get-Content $env:USERPROFILE\.ssh\id_rsa.pub | clip
# Test ssh connection to GitHub
ssh -T git@github.com
```

## Customize PowerShell `$PROFILE`

Add the following to `$PROFILE`:

```powershell
# Import posh-git
Import-Module -Name posh-git
# Start ssh-agent
Start-SshAgent
```

---
