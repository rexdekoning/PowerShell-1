# Get-WindowsProductKey

Get the Windows product key and some usefull informations about the system.

* [view function](https://github.com/BornToBeRoot/PowerShell/blob/master/Module/LazyAdmin/Functions/Get-WindowsProductKey.ps1)
* [view script](https://github.com/BornToBeRoot/PowerShell/blob/master/Scripts/Get-WindowsProductKey.ps1)

## Description

Get the Windows product key from a local or remote system and some informations like Serialnumber, Windows version, Bit-Version etc. from one or more computers.

Remote computers need WinRM enabled. To do this use `winrm quickconfig`.

![Screenshot](Images/Get-WindowsProductKey.png?raw=true "Get-WindowsProductKey")

## Syntax 

### Function

```powershell
Get-WindowsProductKey [[-ComputerName] <String[]>] [[-Credentials] <PSCredential>] [<CommonParameters>]
```

### Script

```powershell
.\Get-WindowsProductKey.ps1 [[-ComputerName] <String[]>] [[-Credentials] <PSCredential>] [<CommonParameters>]
```

## Example

### Function

```powershell
PS> Get-WindowsProductKey

ComputerName   : TEST-PC-01
WindowsVersion : Microsoft Windows 10 Pro
CSDVersion     :
BitVersion     : 64-bit
BuildNumber    : 10586
ProductID      : 00000-00000-00000-00000
ProductKey     : XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
```

### Script

```powershell
PS> .\Get-WindowsProductKey.ps1 -ComputerName TEST-PC-01,TEST-PC-02

ComputerName   : TEST-PC-01
WindowsVersion : Microsoft Windows 10 Pro
CSDVersion     :
BitVersion     : 64-bit
BuildNumber    : 10586
ProductID      : 00000-00000-00000-00000
ProductKey     : XXXXX-XXXXX-XXXXX-XXXXX-XXXXX

ComputerName   : TEST-PC-02
WindowsVersion : Microsoft Windows 10 Pro
CSDVersion     :
BitVersion     : 64-bit
BuildNumber    : 10586
ProductID      : 00000-00000-00000-00000
ProductKey     : XXXXX-XXXXX-XXXXX-XXXXX-XXXXX
```
