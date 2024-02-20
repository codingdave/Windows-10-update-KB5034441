# Windows-10-update-KB5034441
Fix for 2024-01 Security Update for Windows 10 Version 22H2 for x64-based Systems (KB5034441)
Microsoft has provided that script over [here](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/add-update-to-winre?view=windows-11#extend-the-windows-re-partition), but cannot run without and thus fails.

## Changes done
- Lines 96 and 581: changed
```
$WinRELocation.Split('\\')
```
to 
```
$WinRELocation.Split('\')
```
