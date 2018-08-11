# Uninstall Windows 10 Apps
How to uninstall Windows 10 apps (even those built-in) using PowerShell commands.

Reference: https://pureinfotech.com/uninstall-apps-powershell-windows-10/

View apps installed for your account.
```
Get-AppxPackage
```

View apps installed on the machine.
```
Get-AppxPackage -AllUsers
```

Uninstall the app.
```
Get-AppxPackage Microsoft.WindowsCamera | Remove-AppxPackage
```
