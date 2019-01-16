# Uninstall Windows 10 Apps
Remove Windows 10 apps (even those built-in) with PowerShell.

**Tip:** It's much easier to type PowerShell commands in all lowercase. The following commands have been capitalized for your viewing pleasure, but again, it is not required.

That means
```
get-appxpackage
```
will be interpreted the same as
```
Get-AppxPackage
```

## Instructions
View apps installed for your account.
```
Get-AppxPackage
```

View apps installed on the machine.
```
Get-AppxPackage -AllUsers
```

Uninstall specific app.
```
Get-AppxPackage Microsoft.WindowsCamera | Remove-AppxPackage
```

## Common Errors
Users will encounter an error message if the app is part of Windows and unable to be uninstalled on a per-user basis.
Add the `-AllUsers` arguement to remedy this.
```
Get-AppxPackage Microsoft.Wallet -AllUsers | Remove-AppxPackage
```

---

- [Reference 1](https://pureinfotech.com/uninstall-apps-powershell-windows-10)
- [Reference 2](https://www.askvg.com/guide-how-to-remove-all-built-in-apps-in-windows-10/)
