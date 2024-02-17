# Powershell snippets


## Table of kernel modules 
Sys driver files 

```
Get-CimInstance -ClassName Win32_SystemDriver | Select-Object -Property Name,State,DisplayName,Description,PathName | Sort-Object -Property State | Format-Table
```

Inf files
```
Get-WindowsDriver -Online -All | Select-Object -Property Driver,ProviderName,Online,ClassDescription,DriverSignature,OriginalFilename | Sort-Object -Property ProviderName,ClassDescription,Driver | Format-Table
```