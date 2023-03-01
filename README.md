# Windows-PowerShell-Remove-Programs
Uninstall programs from the command line

Run Powershell:

Get list of installed programs:

Get-WmiObject -Class Win32_Product | Select-Object -Property Name

Now Run these commends:

$MyApp = Get-WmiObject -Class Win32_Product | Where-Object{$_.Name -eq "Program Name"}

$MyApp.Uninstall()
