# Windows-10-update-KB5034441
Fix for 2024-01 Security Update for Windows 10 Version 22H2 for x64-based Systems (KB5034441).

## How
Open a PowerShell (classical, PowerShell Core does not work) promt with administrator permissions. Download the script and run it. Be sure to read whats written and follow the guide within. Do on your own risk.

```
.\fix_0x80070643-icrease_WinRE_partition_size.ps1
```

## Why
The "2024-01 Security Update for Windows 10 Version 22H2 for x64-based Systems (KB5034441)" update often fails with error 0x80070643.

Actually the reason for failure seems to be that the WinRE partition is too small to install an BitLocker fix.

The partition needs to changed in a particular way that is so finicky that Microsoft has provided a script to perform necessary actions over [here](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/add-update-to-winre?view=windows-11#extend-the-windows-re-partition). Unfortunately this script cannot run without errors and thus fails.

## Changes done
- Lines 96 and 581: changed
```
$WinRELocation.Split('\\')
```
to 
```
$WinRELocation.Split('\')
```
