# Windows Process Vailidity
How do we discover Normal, abnormal, and Hidden Processes and Services?
``` powershell
Get-Process SMSS,CSRSS,LSASS | Sort -Property Id
```
Do boot processes have descriptions?
``` pwsh
Get-Process | Select Name, Id, Description | Sort -Property Id
```
Where do the system processes and services normally run from? (C:\Windows\System32)
```pwsh
Get-Process | Select Name, Id, Path
```
```powershell
Get-Ciminstance Win32_service | Select Name, Processid, Pathname
```
Are Priority Levels of processes important?
``` pwsh
Get-Process | Select Name, Priorityclass
```
```pwsh
Tasklist /m
```
How would malware use Schedule Task?
```powershell
schtasks /query | more
```
~~~pwsh
Get-ScheduledTask | Select * | Select -First 5
~~~
