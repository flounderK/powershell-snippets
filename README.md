# Powershell snippets


## Table of kernel modules 
```
Get-CimInstance -ClassName Win32_SystemDriver | Select-Object -Property Name,State,DisplayName,Description,PathName | Sort-Object -Property State | Format-Table
```