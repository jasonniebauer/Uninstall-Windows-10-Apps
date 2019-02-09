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

## View Installed Apps
View apps installed for the signed in user account.
```
Get-AppxPackage
```

View apps installed for all users on the machine.
```
Get-AppxPackage -AllUsers
```

## Uninstall Apps
Uninstall apps with the command below where `<NAME>` is the name of the app you wish to remove.
```
Get-AppxPackage <NAME> | Remove-AppxPackage
```

Here is an example of uninstalling Zune Music for the signed in user account.
```
Get-AppxPackage Microsoft.ZuneMusic | Remove-AppxPackage
```

## Common Errors
An error message will be displayed if the app is part of Windows and unable to be uninstalled on a per-user basis. This means that the app must be uninstalled for all users.

Add the `-AllUsers` flag to remedy this.
```
Get-AppxPackage Microsoft.Wallet -AllUsers | Remove-AppxPackage
```

---

- [Reference 1](https://pureinfotech.com/uninstall-apps-powershell-windows-10)
- [Reference 2](https://www.askvg.com/guide-how-to-remove-all-built-in-apps-in-windows-10/)
